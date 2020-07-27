<template>
  <mainLayout>
    <div class="section is-large">
      <h2 class="title">About Me</h2>
      <p>Hi! My name is Wesley Ford. I am a college student majoring in computer science. For three years I have been programming.</p>
    </div>
  </mainLayout>
</template>

<script>
export default {
  metaInfo: {
    title: 'about me',
    meta: [
      {
        name: 'author',
        content: 'Wesley Ford'
      },
      {
        key: 'description',
        name: 'description',
        content: 'Welcome to my about page! This page will help you get to know me better and  learn about what I am doing as a soon to be software engineer.'
      }
    ],
  }
}
</script>
