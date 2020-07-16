<template>
  <div>
    <slot></slot>
    <nav role="navigation" class="navbar is-black" aria-label="main navigation">
      <div class="navbar-brand" style="margin-left: 20px;">
        <a class="navbar-item">
          <img
            src="../assets/logoName.png"
            style="background-color: #19FF11; min-width: 65px;"
          />
        </a>
        <a
          v-on:click="isActiveNavbar"
          role="button"
          class="navbar-burger burger"
          aria-label="menu"
          aria-expanded="false"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
      <div class="navbar-menu">
        <div class="navbar-end" style="margin-right: 25px;">
          <a class="navbar-item" href="/">Home</a>
          <a class="navbar-item" href="/about">About Me</a>
          <a class="navbar-item" href="/projects">My Projects</a>
          <a class="navbar-item" href="/contact">Contact Me</a>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  methods: {
    isActiveNavbar: function(){
      var burger = document.querySelector('.burger')
      var navbar = document.querySelector('.navbar-menu')
      navbar.classList.toggle('is-active')
      burger.classList.toggle('is-active')
    }
  }
}
</script>