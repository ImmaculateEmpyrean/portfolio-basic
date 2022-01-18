<template>
    <section class="hire-me-section">
        <div class="wrapper">
            <h1 class="hero-text dark-mode section-heading">Hire Me!</h1>
            <h2 class="menu-item-text caption large-margin-top">My Specializations Dictate The Kind Of Work I Can Do An Exceptional Job In. </h2>
        </div>
        
        <div class="three-way-grid">
            <div class="left grid-cell">
                <Icon class="icon" :size="iconSize">
                    <Development />
                </Icon>
                <p class="bodyText dark-mode">Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia, saepe similique. Velit necessitatibus incidunt, beatae nam modi, quisquam quidem non quam quibusdam architecto, itaque et.</p>
            </div>
            <div class="center grid-cell"></div>
            <div class="right grid-cell"></div>
        </div>

    </section>
</template>

<style lang="scss" scoped>
@use '@/assets/scss/setting' as *;
@import '@/sections/_sectionCommon.scss';

.hire-me-section{
    background-color: $primary-black;
    min-height: 100vh;
}

.three-way-grid{
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    grid-template-areas: 
        "left"
        "center"
        "right";

    @include for-tablet-portrait-up{
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 1fr;
        grid-template-areas: "left center right";
    }
}

.grid-cell{
    display: flex;
    flex-direction: column;
    align-items: center;
}
.left{
    grid-area: left;
    border: 1px solid red;
}

.center{
    grid-area: center;
    border: 1px solid green;
}

.right{
    grid-area: right;
    border: 1px solid blue;
}

.icon{
    color: $primary-white;
}
</style>

<script>
import { Icon } from '@vicons/utils'
import  Development  from '@vicons/carbon/Development';

export default {
    name: "HireMe Section",
    components:{
        Icon,
        Development
    },
    data(){
        return{
            iconSize: "64"
        }
    }
}
</script>