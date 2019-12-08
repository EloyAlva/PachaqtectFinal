<template>
    <header>
        <LogoHeader></LogoHeader>
        <Contacto></Contacto>
    </header>
</template>

<script>
import LogoHeader from '@/components/Header/LogoHeader'
import Contacto from '@/components/Header/Contacto'

export default {
    name : 'Header',
    components : {
        LogoHeader,
        Contacto
    }
}
</script>

<style>

</style>
