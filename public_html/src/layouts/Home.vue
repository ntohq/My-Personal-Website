<template>
  <div class="layout-documentation page-components">
    <navBar>
      <terminal></terminal>
    </navBar>
    <slot/>
    <Footer></Footer>
  </div>
</template>

<script>
import navBar from '~/components/Navbar.vue'
import terminal from '~/components/terminalHeader.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    navBar,
    terminal,
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
