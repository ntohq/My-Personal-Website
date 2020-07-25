<template>
  <mainLayout>
    <contactForm>
      <div class="section has-background-info box">
        <h2 class="title has-text-white">Ways to contact me</h2>
        <ul style="list-style: decimal; margin-left: 20px;">
          <li><a style="color: #12e800;">Contact Form</a></li>
        </ul>
      </div>
    </contactForm>
  </mainLayout>
</template>

<script>
import contactForm from '~/components/contactForm.vue'

export default {
  components: {
    contactForm
  }
}
</script>

<style>
  contactForm div ul li a {
    color: #12e800;
  }
</style>