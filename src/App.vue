<template>
  <div class="icon">
    <i class="fab fa-git-alt"></i><br>
    <span class="title">Commit Generator</span>
  </div>
  <div class="input">
    <input type="text" id="msg" v-model="messageCommit">
  </div>
  <button class="button" @click="newMessage">Generate Message!</button>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      gitCommit: 'git commit -m "',
      messageCommit: 'git commit -m "Ajuste"'
    }
  },
  methods: {
    newMessage(){
      this.messageCommit = this.messageCommit === this.gitCommit + 'Ajuste"' ? 
      this.gitCommit + 'Outra Mensagem"' : 
      this.gitCommit + 'Ajuste"';
      
    },
  }
}
</script>

<style>
#app {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333;
  margin-top: 60px;
}
.title{
  font-weight: 300;
}
.icon i{
  font-size: 54px;
}
.input input{
  text-align: center;
  margin-top:6%;
  width: 60%;
  padding: 12px 40px;
  border-radius: 5px;
  border:none;
  background-color: #333;
  color: #eee;
  font-size: 1.1rem;
  font-family: 'Fira Code';
}
.message{
  margin-top: 6%;
}
.title{
  font-weight: 600;
}
.button{
  margin-top: 3%;
  padding: 12px 45px;
  border:none;
  border-radius: 12px;
  background-color: #418cd6;
  color:#eee;
  font-size: 1.2rem;
  cursor: pointer;
  outline: none;
  font-weight: 600;
}
</style>
