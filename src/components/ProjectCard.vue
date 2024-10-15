
<script>
export default {
    name: 'ProjectCard',
    props:{
        project: Object
    }
}
</script>
<template >
    <div class="col-12 col-md-5 col-lg-4">
        <div class="card">
          <img :src="project.image != null ? `http://127.0.0.1:8000/storage/${project.image}` : 'https://coffective.com/wp-content/uploads/2018/06/default-featured-image.png.jpg'" alt="" class="card-img-top">
          <div class="card-body">
            <h4 class="card-title">{{project.name}}</h4>
            <p>{{project.summary}}</p>
          </div>
        </div>
      </div>
</template>
<style lang="scss">
    
</style>