<template>
  <div class="main">
    <Pomodro />
    <Settings v-if="show" :show="show" @toggle-show="toggleShow"/>
    <button class="button" @click="onClick">S</button>
  </div>
</template> 

<script>
import Settings from './Settings.vue'
import Pomodro from './Pomodro.vue';
  export default {
    name:'Main',
    components: {
    Settings,
    Pomodro,
    },
    data(){
      return{
        show: false
      }
    },
    methods:{
      onClick(){
        this.show = !this.show
      },
      toggleShow(){
        this.show = !this.show
      }
    }
  }
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  background: #1E213F;
  color: #fff,#EFF1FA;
  font-family: sans-serif;
}
  .main{
    position: relative;
    max-width: 700px;
    height: 100vh;
    padding: 1.2rem;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    color:#EFF1FA;
  }
  .main button{
    color:#EFF1FA;
  }
  .button{
    font-size:22px;
    cursor: pointer;
    border:none;
    outline: none;
    background: transparent;
  }
</style>