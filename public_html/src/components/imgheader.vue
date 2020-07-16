<template>
  <div class="section is-small has-text-right" style="background-color: rgba(40, 38, 38, 0.97); margin-bottom: 0;">
    <b-button type="" style="color: white; background-color: transparent;" @click="close_terminal">X</b-button>
    <p class="title terminal-font has-text-black has-text-left" ><i ref="command">&#62;</i></p><br>
    <p class="title terminal-font has-text-black has-text-left" ref="line"></p>
  </div>
</template>

<script>
var i = 0;
  export default {
    data(){
      return{
        terminalCommand: '> print(welcomeMessage);',
        terminalResponse: 'Welcome to my personal website! Go ahead and take a look around.',
      }
    },
    mounted(){
      this.$nextTick(this.simulatedTyping());
    },
    methods: {
        close_terminal: function(e){
         e.target.parentElement.style.display = "none";
         e.target.parentElement.setAttribute("display", "none");
        },
        simulatedTyping: function(){
          var vm = this;

          if (i < vm.terminalCommand.length) {
            this.$refs.command.innerText = vm.terminalCommand.substr(0, i) + "_";
            i++;
            setTimeout(vm.simulatedTyping, 100);
          } 
          if(i >= vm.terminalCommand.length){
            this.$refs.command.innerText = vm.terminalCommand.substr(0, i)
            this.$refs.line.innerText = vm.terminalResponse;
          }
        },

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