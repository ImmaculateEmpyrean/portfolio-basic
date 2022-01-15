<template>
<div class="app">
    <nav-wrapper />
    <div class="wrapper">
        <HomeSection />
    </div>
</div>
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

.wrapper{
    max-width: 1400px;
    margin: 0 auto; 
}
</style>
