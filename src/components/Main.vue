<template>
    <div class="container-main">
        <div class="box-pan">
            <div class="titulo-pan">
                <h3>Elige que pan deseas</h3>
            </div>
            <div class="productos-pan">
                <div class="item">
                    <div class="caja-img">
                        <img src="@/assets/img-main/pan1.jpg" alt="">
                    </div>
                    <p>Pan crocante</p>
                    <button>Agregar</button>
                    
                </div>
                <div class="item">
                    <div class="caja-img">
                        <img src="@/assets/img-main/pan2.jpg" alt="">
                    </div>
                    <p>Pan clásico</p>
                    <button>Agregar</button>
                    
                </div>
                <div class="item">
                    <div class="caja-img">
                        <img src="@/assets/img-main/pan3.jpg" alt="">
                    </div>
                    <p>Pan Integral</p>
                    <button>Agregar</button>
                </div>
            </div>

        </div>
        <div class="box-carne">
            <div class="titulo-carne">
                <h3>Elige que carne deseas</h3>
            </div>
            <div class="productos-carne">
                <div class="item">
                    <div class="caja-img">
                        <img src="@/assets/img-main/carne-res.jpeg" alt="">
                    </div>
                    <p>Carne de res</p>
                    <button>Agregar</button>
                    
                </div>
                <div class="item">
                    <div class="caja-img">
                        <img src="@/assets/img-main/carne-pollo.jpeg" alt="">
                    </div>
                    <p>Carne de pollo</p>
                    <button>Agregar</button>
                </div>
                
            </div>
        </div>
        <div class="box-papas">

        </div>   
        <div class="box-papas">

        </div>   
        <div class="box-creams">

        </div>
    </div>
</template>

<script>
export default {
name : 'Main'
}
</script>

<style>
.container-main{
    display: grid;
    grid-gap: 20px;
    max-width: 1000px;
    width: 100%;
    margin-top: 40px
    
}
.productos-pan{
    max-width: 1000px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr;
    grid-gap: 20px;
}
.box-pan{
    display: flex;
    flex-direction: column;
    border: 1px solid #d66d27;
    padding: 10px 20px;
    align-items: center;

}
.titulo-pan h3{
    background: #d66d27;
    height: 40px;
    color: #ffffff
}

.container-main img{
    max-width: 100%;
    border-radius: 50%;
    
}
.box-carne{
    display: flex;
    flex-direction: column;
    border: 1px solid #d66d27;
    padding: 20px;
    align-items: center;

}
.productos-carne{
    max-width: 1000px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 50px
}
.item{
    border: 1px solid #ffb500;
    border-radius: 6px;
    width: 100%;
    padding: 10px;
    box-sizing: border-box;
}

@media only screen and (max-width: 991px){
    .productos-pan{
        grid-template-columns: 1fr 1fr;
    }
    }
</style>
