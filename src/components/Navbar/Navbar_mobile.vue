<template>
    This is the nav-bar on mobile
</template>

<script>
export default {
    name: "Navbar_mobile"
}
</script>

<style lang="scss" scoped>
@use './_Navbar_variables.scss' as navVar;

nav{
    height: navVar.$height;
}
</style>