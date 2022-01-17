<template>
    <div class="project-card">
        <h1 class="title-text center">{{title}}</h1>
        <img :src="image" :alt="imageAlt">
        <slot name="projectDescription"/>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Et ipsum adipisci eum libero? Numquam dolorem officia doloribus itaque reiciendis dolores! Accusamus id necessitatibus ratione mollitia, ducimus porro sit veniam, sapiente nostrum rerum blanditiis illo quas molestias est non odit recusandae consectetur ad. Ratione eveniet in quasi nemo provident odit earum!</p>

        <div class="buttons">
            <a :href="liveLink" class="button">
                <Icon>
                    <BranchFork24Regular />
                </Icon>
                Live Version
            </a>
            <a :href="srcLink" class="button">
                <Icon>
                    <OpenOutline />
                </Icon>
                Source
            </a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '@/assets/scss/setting' as *;

.title-text{
    font-family: sans-serif;
    &.center{
        text-align: center;
    }
}

.project-card{
    margin: var(--spacing-large);
    padding: var(--spacing-normal);
    
    background-color: $primary-white;
    box-shadow: 0px 0px 4px 5px $primary-white;

    display: flex;
    flex-direction: column;
    row-gap: var(--spacing-normal);
}

.left,
.right{
    text-align: center;

    @include for-desktop-up{
        text-align: left;
    }
}

img{
    width: 100%;
}

.buttons{
    display: flex;
    justify-content: space-between;
}

.button{
    display: flex;
    flex-direction: row;
    column-gap: var(--spacing-normal);
    align-items: center;

    text-decoration: none;
    color: $primary-white;
    background-color: $primary-black;
    padding: var(--spacing-small) var(--spacing-normal);

    border-radius: 2px;
}
</style>

<script>
import { Icon } from '@vicons/utils'
import { BranchFork24Regular } from '@vicons/fluent';
import { OpenOutline } from '@vicons/ionicons5';

export default {
    name: "Project Card",
    components:{
        Icon,
        BranchFork24Regular,
        OpenOutline
    },
    props:{
        title:{
            type: String,
            default: "Project Title"
        },
        image:{
            type:String,
            default: "https://via.placeholder.com/200"
        },
        imageAlt:{
            type:String,
            default: "project-image"
        },

        liveLink:{
            type:String,
            default:"https://www.google.com"
        },
        srcLink:{
            type:String,
            default:"https://www.google.com"
        },
    }
}
</script>