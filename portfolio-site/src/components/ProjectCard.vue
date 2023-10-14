<template>
  <div class="project-card hover-grow" :style="{background: 'linear-gradient(transparent, #222), no-repeat center url(' + imagePath + ')'}">
    <div class="project-card-info">
        <h3>{{ project.name }}</h3>
        <p>{{ project.summary }}</p>
    </div>    
  </div>
</template>

<script>
export default {
    props: ['project'],
    computed: {
        imagePath() {
            return '/images/projects/covers/' + this.project.coverImage;
        }
    }
}
</script>

<style>
.project-card {
    width: 300px;
    height: 400px;
    background-color: #333;
    box-shadow: 5px 5px 5px #2226;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
}
</style>