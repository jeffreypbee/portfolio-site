<template>
  <div class="home">
    <h2>Projects</h2>
    <ProjectCards :projects="projects" />
  </div>
</template>

<script>
import ProjectCards from '../components/ProjectCards.vue'

export default {
  name: 'HomeView',
  components: {
    ProjectCards
  },
  data() {
    return {
      projects: [
        {
          name: 'Minesweeper',
          link: 'https://jeffreypbee.github.io/minesweeper/',
          github: 'https://github.com/jeffreypbee/minesweeper',
          summary: 'A recreation of Minesweeper',
          coverImage: 'minesweeper.png'
        }
      ]
    }
  }
}
</script>
