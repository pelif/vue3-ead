<template>
  <div>
    <div class="pageTitle">
      <span class="title">{{ title }}</span>
      <span class="dots">
          <span></span>
          <span></span>
          <span></span>
      </span>
    </div>

    <div class="content">
      <ul class="listCourses">
          <card-course 
            :title="'Curso de Laravel com Vue.js'"
            :image="''"
            :bgName="'laravel'">
          </card-course>       
      </ul>
    </div>
  </div>      
</template>

<script>
import CardCourse from './components/CardCourse.vue';

export default {
  name: "HomeView",
  components: {
    CardCourse
  }
};
</script>
