<template>
    <template v-if="false">
        <Navbar_mobile />
    </template>

    <template v-if="true">
        <Navbar_desktop />
    </template>
</template>

<script>
import Navbar_desktop from '@/components/Navbar/Navbar_desktop.vue';
import Navbar_mobile  from '@/components/Navbar/Navbar_mobile.vue'; 

export default {
    name: "NavBar",
    components:{
        Navbar_desktop,
        Navbar_mobile
    }
}
</script>

<style lang="scss" scoped>
@use '@/assets/scss/setting' as *;

</style>