<template>
  <mainLayout>
    <section class="hero is-medium" style="margin-top: 20px; margin-bottom: 0px;">
      <div class="hero-body has-text-centered" style="margin-bottom: 0px; padding-bottom: 50px;">
        <h1 class="title is-1">My Projects</h1>
        <p class="subtitle"><i>A place to showcase what I do.</i></p>
      </div>
    </section>
    <myProjectsVue></myProjectsVue>
  </mainLayout>
</template>

<script>
import myProjectsVue from '~/components/my-projects.vue'

export default {
 metaInfo(){
   return{
     title: 'my projects'
   }
 },
 components:{
   myProjectsVue
 }
}
</script>