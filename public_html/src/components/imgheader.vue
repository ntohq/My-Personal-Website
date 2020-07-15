<template>
  <div class="section is-small has-text-right" style="background-color: rgba(38, 38, 38, 0.97); margin-bottom: 0;">
    <b-button type="is-warning" @click="close_terminal">X</b-button>
    <p class="title terminal-font has-text-black has-text-left" ref="command">&#62;</p><br>
    <p class="title terminal-font has-text-black has-text-left" ref="line"></p>
  </div>
</template>

<script>
  export default {
    data(){
      return{
        terminalCommand: '> print(intro);',
        terminalResponse: '>> "Welcome to my personal website"',
      }
    },
    mounted(){
      this.$nextTick(this.simulatedTyping());
    },
    methods: {
        close_terminal: function(e){
         e.target.parentElement.style.display = "none";
        },
        simulatedTyping: function(){
          var vm = this;
          

          for(let i = 1; i < vm.terminalCommand.length + 1; i++){
            this.$refs.command.innerText = vm.terminalCommand.substr(0, i) + "_";
          }

          for(let i = 1; i < vm.terminalResponse.length + 1; i++){
            this.$refs.line.innerText = vm.terminalResponse.substr(0, i);
          }
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