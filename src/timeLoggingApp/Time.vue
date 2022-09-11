<template>
  <div class="time">
    <div class="sec">
      <!-- <svg id="svg" width="240" height="240"> -->
        20:30
      <!-- </svg> -->
    </div>
  </div>
</template>

<script>
  export default { 
    name: 'Time',
  }
</script>

<style scoped>
  .time{
    position: relative;
    overflow: hidden;
    width: 300px;
    height: 300px;
    background-color: #1E213F;
    box-shadow:-1em -1em 2em  #353a70, 2em 2em 3em  rgba(0, 0, 0, 0.5);
     /* -2px -2px 15px 5px rgb(255, 255, 255,); */
    border-radius: 50%;
    left: 50%;
    transform: translateX(-50%);
  }
  .sec{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    width: 260px;
    height: 260px;
    border-radius: 50%;
    background-color: rgba(0, 0, 0, 0.4);
    box-shadow: -2em -2em 3em  rgba(0, 0, 0, 0.5),inset 2em 2em 3em  rgba(0, 0, 0, 0.1);
  }
  svg{
    color:#fff;
    background:red;
  }
  span{
    margin: 0;
    padding: 0;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    font-size: 4em;
    color: #fff;
  }
</style>