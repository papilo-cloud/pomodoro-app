<template>
  <div class="settings">
    <form>
      <div class="h2">
        <h2>Settings</h2>
      </div>
      <h4>Time (minutes)</h4>
      <div class="number">
        <div class="num">
        <label>
          pomodoro <br>
          <input type="number" min="15" max="25" value="25" aria-colspan="18">
        </label>
        </div>
        <div class="num">
        <label>
          short break <br>
          <input type="number" min="1" max="5" value="5">
        </label>
        </div>
        <div class="num">
        <label>
          long break <br>
          <input type="number" min="5" max="15" value="15">
        </label>
      </div>
      </div>
      <div class="check1">
        <label>
          <input type="checkbox">
        </label>
        <label>
          <input type="checkbox">
        </label>
        <label>
          <input type="checkbox">
        </label>
      </div>
      <div class="check2">
        <label>
          <input type="checkbox">
        </label>
        <label>
          <input type="checkbox">
        </label>
        <label>
          <input type="checkbox">
        </label>
      </div>
    </form>
    <h1>S</h1>
  </div>
</template>

<script>
  export default {
    name: 'Settings',
  }
</script>

<style scoped>
  
  .settings{
    color:#000;
    padding: 1.2rem;
    position: absolute;
    width: 100%;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
  }
  .h2{
    position: relative;
    margin: 0;
    padding: 0;
  }
  .settings h2, h4{
    margin-bottom: 1.2rem;
  }
  .number{
    display: flex;
    flex-wrap: wrap;
  }
  .number .num{
    flex: 400px;
  }
  form{
    width: 100%;
     background-color: #fff;
     padding: 20px;
     border-radius: 15px;
  }
  .num label{
    width: 100%;
    display: flex;
    justify-content: space-between;
    color: #777;
    align-items: center;
  }
  .num input{
    padding: 8px;
    width: 170px;
    margin: 5px 0;
    border:none;
    outline:none;
    border-radius:8px;
    background:#EFF1FA;
    font-weight: bold;
  }
  @media screen and (min-width:700px) {
    .number{
      justify-content: space-between;
    }
    .number .num{
    flex:1 200px;
  }
    .num label{
      display: block;
    }
  }

</style>