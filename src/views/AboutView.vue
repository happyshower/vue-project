<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="increment">{{ count }}</button>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
}
</style>

<script setup lang="ts">
import { ref } from 'vue'

var count = ref(0)

var increment = ()=> {
  // 在 JavaScript 中需要 .value
  count.value++
}
</script>
