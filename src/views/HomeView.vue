<script setup lang="ts">
import Side from '../components/Side.vue'
import Conversation from '../components/Conversation.vue'
</script>

<template>
  <main class="home">
    <Side style="flex: 2" />
    <Conversation style="flex: 10" />
  </main>
</template>

<style>
.home {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}
</style>
