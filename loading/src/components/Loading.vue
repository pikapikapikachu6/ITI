<script setup>
let show = $ref(true)
</script>

<template>
  <div class="space-x-4 ...">
    <div class="inline-block">
      <div class="container w-20 h-20 justify-center items-center" v-if="show">
        <img src="/loading.svg" class="absolute w-20">
      </div>
    </div>
    <div class="inline absolute top-7">正在加载中...</div>
  </div>
</template>