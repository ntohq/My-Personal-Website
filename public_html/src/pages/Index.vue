<template>
  <Layout>
    <greetings style="margin-left: auto; margin-right: auto; max-width: 125em;"></greetings>
    <quickView style="margin-left: auto; margin-right: auto; max-width: 125em;"></quickView>
  </Layout>
</template>

<script>
import greetings from '~/components/greeting.vue'
import quickView from '~/components/quickPreviewTiles.vue'
export default {
  metaInfo: {
    title: 'home'
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
