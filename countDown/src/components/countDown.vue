<template>
  <p>Countdown Timer</p>
  <input class="text" v-model="data" />
  <button @click="countDownStart()">start</button>
  <button @click="reset()">end</button>
  <p>{{time}}</p>
</template>

<script setup>
  import {ref} from '@vue/reactivity'
  const data = ref()
  const left = ref()
  const time = ref("00:00:00")
  const hour = ref(0)
  const minute = ref(0)
  const seconds = ref(0)

  const countDownStart = () => {
    left.value = data.value
    const countdown = setInterval(() => {
      change();
      left.value --;
      if (left.value <= 0) {
        reset();
        clearInterval(countdown);
      }
    }, 1000)
  }

  const change = () => {
    hour.value = Math.floor(left.value / 60 / 60);
    minute.value = Math.floor(left.value / 60 % 60);
    seconds.value = Math.floor(left.value % 60);
    time.value = `${hour.value < 10 ? '0' : ''}${hour.value} : ${minute.value < 10 ? '0' : ''}${minute.value} : ${seconds.value < 10 ? '0' : ''}${seconds.value}`
  }

  const reset = () => {
    data.value = 0
    left.value = 0
    time.value = "00:00:00"
    hour.value = 0
    minute.value = 0
    seconds.value = 0
  }
</script>

<style>
</style>
