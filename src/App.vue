<template>
<div class="app">
    <Navbar />
    <HomeSection />
    <PortfolioSection />
</div>
</template>

<script>
import HomeSection from '@/sections/HomeSection.vue';
import PortfolioSection from '@/sections/PortfolioSection.vue';

import Navbar from '@/components/Navbar/Navbar.vue';

export default {
    name: 'App',
    components:{
        HomeSection,
        PortfolioSection,
        Navbar,
    },
    mounted(){
        console.log('app started')
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
