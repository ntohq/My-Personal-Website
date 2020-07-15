<template>
  <div class="section is-small" style="background-color: rgba(38, 38, 38, 0.97); margin-bottom: 0;">
    <b-button type="is-warning" @click="close_terminal">X</b-button>
    <p class="title terminal-font has-text-black" >&#62;
    </p>
  </div>
</template>

<script>
  export default{
    created(){
      //draw_line();
    },
    methods: {
        close_terminal: function(e){
         e.target.parentElement.style.display = "none";
        }
    }
  }
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@500&display=swap');

.terminal-text {
  font-family: 'Inconsolata', monospace;
  margin-right: 0;
}
</style> 