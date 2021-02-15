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
    title: 'home',
    meta: [
      {
        name: 'author',
        content: 'Wesley Ford'
      },
      {
        key: 'description',
        name: 'description',
        content: 'Welcome! You have found my personal website! Go ahead and take a look around.'
      },
      {
        key: 'keywords',
        name: 'keywords',
        content: 'Wesley Ford, developer, homepage, info, tech, software, programmer'
      }
    ],
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
