<template>
  <mainLayout>
    <section class="section">
      <h2 class="title is-2">
        {{ $page.post.title }}
      </h2>
      <b-tag rounded>{{ date_published }}</b-tag>
      <p v-html="$page.post.content"></p>
    </section>
  </mainLayout>
</template>

<page-query>
query Post ($path: String!) {
  post: post (path: $path) {
    title
    slug
    published
    content
  }
}
</page-query>

<script>
export default {
  name: 'Post',
  metaInfo(){
    return {'title': this.$page.post.slug}
  },
  computed:{
    date_published(){
      return this.$page.post.published;
    }
  }
}
</script>