<template>
     <div class="img-logo">
         <img src="@/assets/logoHeader.jpeg" alt="" class="img-logo-header">
     </div>

     
</template>

<script>

export default {
    name : 'LogoHeader'
}
</script>

<style>
    .img-logo-header{
        max-width: 100%;
    }

    @media only screen and (max-width: 991px){
        .img-logo-header{
        height: 44px;
    }
    }
</style>
