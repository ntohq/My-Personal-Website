<template>
  <Layout>
    <greetings></greetings>
  </Layout>
</template>

<script>
import greetings from '~/components/greeting.vue'

export default {
  metaInfo: {
    title: 'Home'
  },
  components: {
    greetings
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
