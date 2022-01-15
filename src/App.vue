<template>
<div class="app">
    <Navbar :menuButtonSelected="menuButtonSelected" />
    <div class="wrapper">
        <HomeSection />
    </div>
</div>
</template>

<script>
import HomeSection from '@/sections/HomeSection.vue';
import Navbar from '@/components/Navbar/Navbar.vue';

export default {
    name: 'App',
    components:{
        HomeSection,
        Navbar,
    },
    data(){
        return{
            menuButtonSelected: "home"
        }
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
