<template>
  <div class="layout-documentation page-components">
    <navBar></navBar>
    <slot/>
    <Footer></Footer>
  </div>
</template>

<script>
import navBar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    navBar,
    Footer
  }
}
</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>