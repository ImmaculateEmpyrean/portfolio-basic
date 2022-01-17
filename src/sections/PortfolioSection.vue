<template>
    <section class="portfolio-section">
        <div class="wrapper">
            <h1 class="hero-text dark-mode">Projects</h1>
            <h2 class="menu-item-text dark-mode">A list of my most important projects for your viewing pleasure.</h2>
            <a class="menu-item-text dark-mode" href="#">Click here for the full list</a>

            <div class="projects">
                <ProjectCard 
                    style="grid-area: 'project-1'"
                    title="Full Stack Shopping Website"
                    image="https://via.placeholder.com/150"
                    imageAlt="the placeholder image"
                    liveLink="#" srcLink="#"
                />
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '@/assets/scss/setting' as *;

.portfolio-section{
    min-height: 100vh;
    margin: 0 auto;
    background-color: $primary-black;

    display: flex;
    flex-direction: column;
    justify-content: center;
}
.wrapper{
    max-width: 1400px;
    width: 100%;

    display: flex;
    flex-direction: column;
    justify-content: center;
    
    height: 100%;
}
.projects{
    margin: 0 var(--spacing-normal);

    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 1fr 1fr 1fr 1fr 1fr;
    grid-template-areas: 
        "project-1",
        "project-2",
        "project-3",
        "project-4",
        "project-5",
        "project-6";

    @include for-tablet-portrait-up{
        grid-template-columns: 1fr 1fr;
        grid-auto-rows: 1fr 1fr 1fr;
        grid-template-areas: 
            "project-1 project-2",
            "project-3 project-4",
            "project-5 project-6";
    }

    @include for-desktop-up{
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        grid-template-areas: 
            "project-1 project-2 project-3",
            "project-4 project-5 project-6";
    }
}
</style>

<script>
import ProjectCard from '@/components/ProjectCard.vue';

export default {
    name: "Portfolio Section",
    components:{
        ProjectCard
    }
}
</script>