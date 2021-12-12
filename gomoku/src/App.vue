<script setup>
import {ref} from '@vue/reactivity'
const current = ref(1)

const item = ref({
    empty: true,
    player1: false
})

const change = () => {
  if (current.value == 1) {
    if (item.value.empty) {
      item.value.empty = false
      if (!item.value.player1) {
        item.value.player1 = true
      }
    }
    current.value = 2
  } else {
    if (item.value.empty) {
      item.value.empty = false
      item.value.player1 = false
    }
    current.value = 1
  }
}
</script>

<template>
  <p> 五子棋游戏 </p>
  <button @click="start">start</button>
  <button @click="restart()">restart</button>
  <p> player1 </p>
  <p> player2 </p>

  <p>{{item.empty}}</p>
  <div class="container">
    <template v-for="n in 19">
      <template v-for="m in 19">
        <div :class="item.empty ? 'item' : (item.player1 ? 'item1' : 'item2')" @click="change()"></div>
      </template>
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

  .container .item1{
    border: 1px solid black;
    background: red;
  }

  .container .item2{
    border: 1px solid black;
    background: blue;
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


