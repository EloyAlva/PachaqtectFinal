<template>
    <div class="container-all">
        <input type="radio" id="1" name="image-slide" hidden>
        <input type="radio" id="2" name="image-slide" hidden>
        <input type="radio" id="3" name="image-slide" hidden>

        <div class="slide">
            <div class="item-slide">
                <img src="@/assets/img-aside/slider1.jpg" alt="">
            </div>
            <div class="item-slide">
                <img src="@/assets/img-aside/slider2.jpg" alt="">
            </div>
            <div class="item-slide">
                <img src="@/assets/img-aside/slider3.jpg" alt="">
            </div>
        </div>

        <div class="pagination">
            <label class="pagination-item" for="1">
                <img src="img/slider1.jpg" alt="">
            </label>
            <label class="pagination-item" for="2">
                <img src="img/slider2.jpg" alt="">
            </label>
            <label class="pagination-item" for="3">
                <img src="img/slider3.jpg" alt="">
            </label>
        </div>
    </div>
</template>

<script>
export default {
    name : 'Aside'
}
</script>

<style>
    .home{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 30px;
}

.container-all img{
    max-width: 100%;
}

.container-all{
    position: relative;
    max-width: 1000px;
    width: 100%;
    border-radius: 6px;
    overflow: hidden;
}

.slide{
    display: flex;
    transform: translate3d(0, 0, 0);
    transition: all 600ms;
    animation-name: autoplay;
    animation-duration: 6.5s;
    animation-direction: alternate;
    animation-fill-mode: forwards;
    animation-iteration-count: infinite;
}

.item-slide{
    position: relative;
    display: flex;
    flex-direction: column;
    flex-shrink: 0;
    flex-grow: 0;
    max-width: 100%;
}

.pagination{
    position: absolute;
    bottom: 20px;
    left: 0;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    width: 100%;
}

.pagination-item{
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 2px solid white;
    width: 16px;
    height: 16px;
    border-radius: 4px;
    overflow: hidden;
    cursor: pointer;
    background: rgba(255, 255, 255, 0.5);
    margin: 0 10px;
    text-align: center;
    transition: all 300ms;
}

.pagination-item:hover{
    transform: scale(2);
}

.pagination-item img{
    display: inline-block;
    max-width: none;
    height: 100%;
    transform: scale(1);
    opacity: 0;
    transition: all 300ms;
}

.pagination-item:hover img{
    opacity: 1;
    transform: scale(1);
}


input[id="1"]:checked ~ .slide{
    animation: none;
    transform: translate3d(0, 0, 0);
}

input[id="1"]:checked ~ .pagination .pagination-item[for="1"]{
    background: #fff;
}

input[id="2"]:checked ~ .slide{
    animation: none;
    transform: translate3d(calc(-100% * 1), 0, 0);
}

input[id="2"]:checked ~ .pagination .pagination-item[for="2"]{
    background: #fff;
}


input[id="3"]:checked ~ .slide{
    animation: none;
    transform: translate3d(calc(-100% * 2), 0, 0);
}

input[id="3"]:checked ~ .pagination .pagination-item[for="3"]{
    background: #fff;
}


@keyframes autoplay{
    33%{
        transform: translate3d(calc(-100% * 0), 0, 0);
    }
    
    66%{
        transform: translate3d(calc(-100% * 1), 0, 0);
    }
    
    100%{
        transform: translate3d(calc(-100% * 2), 0, 0);
    }
}
</style>
