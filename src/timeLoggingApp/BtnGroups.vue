<template>
  <div class="butn">
    <button >{{text}}</button>
  </div>
</template>

<script>
  export default {
    name: 'Settings', 
    props:{
      color: String,
      text: String
    }
  }
</script>

<style scoped lang="css">

  button{
    padding: 12px;
    color:#fff;
    font-size: 18px;
    letter-spacing: 1px;
    border-radius:25px;
    border:none;
    outline:none;

  }

</style>