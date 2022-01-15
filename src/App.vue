<template>
    <nav-wrapper />
    <HomeSection />
</template>

<script>
import HomeSection from '@/sections/HomeSection.vue';
import NavWrapper from '@/components/Navbar/NavWrapper.vue';

export default {
    name: 'App',
    components:{
        HomeSection,
        NavWrapper,
    }
}
</script>

<style lang="scss">
@use '@/assets/scss/setting' as *;

</style>
