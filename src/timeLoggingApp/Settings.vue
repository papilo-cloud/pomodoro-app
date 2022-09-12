<template>
  <div class="settings">
    <form>
      <div class="h2">
        <h2>Settings</h2>
        <button @click="$emit('toggle-show')">&times;</button>
      </div>
      <h6>Time (minutes)</h6>
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
        <h6>Font</h6>
        <div>
          <label>
          <input type="radio" name="radi" v-model="col" value="red">
          <span class="check">Aa</span>
        </label>
        <label>
          <input type="radio"  v-model="col" value="brown">
          <span class="check">Aa</span>
        </label>
        <label>
          <input type="radio"  v-model="col" value="blue">
          <span class="check">Aa</span>
        </label>
        </div>
      </div>
      <div class="check2">
        <h6>color</h6>
        <div>
          <label>
          <input type="radio">
          <span class="check"></span>
        </label>
        <label>
          <input type="radio">
          <span class="check"></span>
        </label>
        <label>
          <input type="radio">
          <span class="check"></span>
        </label>
        </div>
      </div>
    </form>
    <h1 v-for="thm in theme" :key="thm">{{thm.color}}</h1>
  </div>
</template>

<script>
  export default {
    name: 'Settings',
    props:{
      show:Boolean
    },
    data() {
      return{
        theme:[],
        col:''
      }
    },
    method: {
      onSubmit(e){
        e.preventDefault()
      }
    }
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
    padding: 1.2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1.2rem;
  }
  .h2 button{
    border:none;
    outline:none;
    font-size: 32px;
    background:transparent;
    cursor: pointer;
  }
  .h2::after{
    content:'';
    position: absolute;
    height: 4px;
    width: 100%;
    background: #EFF1FA;
    bottom: 0;
    left: 0;
  }
   h2, h4{
    padding: 0;
    margin: 0;
  }
  .settings h6{
    text-align: center;
    font-weight: lighter;
    letter-spacing: 2px;
    text-transform: uppercase;
  }
  form .number{
    position: relative;
    display: flex;
    flex-wrap: wrap;
    padding: 1.2rem;
    overflow: hidden;
  }
  .number::before{
    content:'';
    position: absolute;
    height: 3px;
    background: #EFF1FA;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 90%;
  }
  .number .num{
    flex: 400px;
  }
  form{
    width: 100%;
     background-color: #fff;
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
  .check1, .check2 {
    position: relative;
    padding: .5rem 1.2rem;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: space-between;
    margin-bottom: 0;
  }
  .check1 > div{
    margin: 0;
    padding: 0;
  }
  .check1 label, .check2 label{
    position: relative;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    margin: 10px;
    display: inline-block;
    cursor:pointer;

  }
   .check{
    position: absolute;
    top: 0;
    left:0;
    width: 100%;
    height: 100%;
        background: #EFF1FA;
        border-radius: 50%;
    /* text-align: center; */
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .check2 .check{
        background: transparent;
  }
  .check2 .check::after{
    content:'';
    position:absolute;
    display:none
  }
  .check2 input:checked ~ .check::after{
    display: block;
  }
  .check2 .check::after{
    left: 15px;
    top: 10px;
    width: 5px;
    height: 14px;
    border:solid #fff;
    border-width: 0 3px 3px 0;
    transform: rotate(45deg);
  }
  .check1 label input:checked ~ .check, .check2 label input:checked ~ .check {
    background:#161932;
    color: #fff;
  }
  .check2 label:nth-child(1){
    background: #F87070;
  }
  .check2 label:nth-child(2){
    background: #70F380;
  }
  .check2 label:nth-child(3){
    background: #70f3f8;
  }
  .check1 label input, .check2 label input{
    opacity: 0;
  }
  @media screen and (min-width:700px) {
    .number{
      justify-content: space-evenly;
    }
    .number .num{
    flex: 200px;
  }
    .num label{
      display: block;
    }
    .check1, .check2 {
   
    flex-direction: unset;
  }
  }

</style>