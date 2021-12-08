<script setup>
</script>

<template>
  <p> 五子棋游戏 </p>
  <button @click="start">start</button>
  <button @click="restart()">restart</button>
  <p> player1 </p>
  <p> player2 </p>

  <div class="container">
    <template v-for="n in 19">
      <div class="item" v-for="m in 19"></div>
    </template>
  </div>
    
</template>

<style>
  .container {
    width: 400px;
    height: 400px;
    margin: auto;
    background: white;
    display: grid;
    grid-template-columns: repeat(19, 1fr);  
    grid-template-rows: repeat(19, 1fr);  
  }

  .container .item{
    border: 1px solid black;
    background: white;
  }

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
