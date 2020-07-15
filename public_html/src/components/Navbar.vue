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
        <div class="navbar-end" style="margin-right: 0px;">
          <a class="navbar-item" href="/">Home</a>
          <a class="navbar-item" href="/">Posts</a>
          <div class="navbar-item has-dropdown is-hoverable">
            <a class="navbar-link is-arrowless">Projects</a>
            <div class="navbar-dropdown is-right">
              <a class="navbar-item">p5 Projects</a>
              <a class="navbar-item">.Net Projects</a>
              <a class="navbar-item">Python Projects</a>
            </div>
          </div>
          <div class="navbar-item has-dropdown is-hoverable">
            <a class="navbar-link is-arrowless" href="/api">Apis</a>
            <div class="navbar-dropdown is-right">
              <a class="navbar-item">Analyst-Server</a>
              <a class="navbar-item">Ntohq-Server</a>
            </div>
          </div>
          <div class="navbar-item has-dropdown is-hoverable">
            <a href="#" class="navbar-link image is-64x64 is-arrowless">
              <img :src="userImage" />
            </a>
            <div class="navbar-dropdown is-right" style="margin-right: 5px;">
              <div v-if="userLogedOn">
                <a class="navbar-item">Settings</a>
                <a v-on:click="logOut" class="navbar-item">Log Out</a>
              </div>
              <div v-else>
                <a class="navbar-item" v-on:click="userLogIn">Log In</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>