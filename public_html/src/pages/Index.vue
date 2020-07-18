<template>
  <Layout>
    <greetings style="margin-left: auto; margin-right: auto; max-width: 150em;"></greetings>
    <quickView style="margin-left: auto; margin-right: auto; max-width: 150em;"></quickView>
  </Layout>
</template>

<script>
import greetings from '~/components/greeting.vue'
import quickView from '~/components/quickPreviewTiles.vue'
export default {
  metaInfo: {
    title: 'Home'
  },
  components: {
    greetings,
    quickView
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
