<template>
  <div class="layout-documentation page-components">
    <navBar>
      <imageHeader></imageHeader>
    </navBar>
    <slot/>
  </div>
</template>

<script>
import navBar from '~/components/Navbar.vue'
import imageHeader from '~/components/imgheader.vue'
export default {
  components: {
    navBar,
    imageHeader
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

<style>
body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
}
</style>
