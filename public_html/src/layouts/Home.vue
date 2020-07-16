<template>
  <div class="layout-documentation page-components">
    <navBar>
      <imageHeader></imageHeader>
    </navBar>
    <slot/>
    <Footer></Footer>
  </div>
</template>

<script>
import navBar from '~/components/Navbar.vue'
import imageHeader from '~/components/imgheader.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    navBar,
    imageHeader,
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
