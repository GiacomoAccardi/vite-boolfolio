<script>
import ProjectCard from '../components/ProjectCard.vue';
import axios from 'axios';

export default {
  components: {
      ProjectCard
    },
  data(){
    return {
      projects: []
    }
  },
  methods:{
    getAllProjects(){
      axios.get('http://127.0.0.1:8000/api/projects').then((res) => {
       this.projects = res.data.results;
      });
    }
  },
  created(){
    this.getAllProjects();
  }
}
</script>

<template>
    <div class="bg-jumbo p-4">
        <div class="col-12">
            <h1 class="text-center text-white">Elenco progetti</h1>
        </div>
    </div>
  <div class="container mt-4">
    <div class="row">
      <div class="col-12">
        <div class="row gy-4">
          <ProjectCard v-for="proj in projects" :key="proj.id" :project="proj"/>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
</style>