<template>
  <mainLayout>
    <section class="section" style="margin-left: auto; margin-right: auto; max-width: 125em;">
      <h2 class="title is-1" style="margin-bottom: 10px;">BLOG</h2>
      <b-tag type="is-primary" rounded style="margin-bottom: 10px;">My Tech Blog</b-tag>
      <section class="section box" 
      v-for="{ node: { title, published, slug, content } } in $page.allPost.edges"
      :key="slug">
      <header>
        <h2 class="title is-2">
          {{ title }}
        </h2>
        <span class="">{{ published }}</span>
      </header>
      <p v-html="content.split('</p>')[0]" style="margin-bottom: 10px;"></p>
      <g-link
          class="button is-primary is-outlined"
          :to="`/blog/${slug}`"
        >
          CONTINUE READING
        </g-link>
      </section>
      <section>
        <h2 class="title is-6">
          Page {{ $page.allPost.pageInfo.currentPage }}
        </h2>
        <div>
          <g-link
            class="button is-primary is-inverted is-outlined"
            :to="previousPagePath"
            v-show="$page.allPost.pageInfo.currentPage > 1"
          >
            PREVIOUS PAGE
          </g-link>
          <g-link
            class="button is-primary is-inverted is-outlined"
            :to="nextPagePath"
            v-show="
              $page.allPost.pageInfo.currentPage <
                $page.allPost.pageInfo.totalPages
            "
          >
            NEXT PAGE
          </g-link>
        </div>
      </section>
    </section>
  </mainLayout>
</template>

<page-query>
query ($page: Int) {
  allPost(perPage: 2, page: $page) @paginate {
    pageInfo {
      totalPages
      currentPage
    }
    edges {
      node {
        title
        subtitle
        slug
        published
        content
      }
    }
  }
}
</page-query>

<script>
export default {
    metaInfo:{
      title: 'blog',
      keywords:'wesley ford, blog, wesley ford post, dev news, ntohq blog'
    },
    name: 'MyBlog',
    computed: {
      previousPagePath() {
        let previousPage = this.$page.allPost.pageInfo.currentPage - 1
        if (previousPage < 2) {
          return '/blog'
        } else {
          return `/blog/${previousPage}`
        }
      },
      nextPagePath() {
        return `/blog/${this.$page.allPost.pageInfo.currentPage + 1}`
      },
    }
}
</script>