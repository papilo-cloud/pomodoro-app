<template>
  <div class="main">
    <Pomodro />
    <Settings />
  </div>
</template> 

<script>
import Settings from './Settings.vue'
import Pomodro from './Pomodro.vue';
  export default {
    name:'Main',
    components: {
    Settings,
    Pomodro
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
  color: #fff,#161932,#EFF1FA;
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
    color:red
  }
</style>