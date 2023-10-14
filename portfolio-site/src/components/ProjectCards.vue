<template>
    <div id="project-cards">
        <ProjectCard v-for="(project, index) in projects" :key="`project-${index}`" :project="project" />
    </div>  
</template>

<script>
import ProjectCard from '../components/ProjectCard.vue'

export default {
    props: ['projects'],
    components: {
        ProjectCard
    }
}
</script>

<style>
#project-cards {
    padding: 10px;
    display: flex;
    gap: 10px;
    justify-content: space-around;
}
</style>