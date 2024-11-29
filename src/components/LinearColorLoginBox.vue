<template>
  <div class="login">
    <div class="bg-box" :style="style">
      <div class="rotate-box"></div>
    </div>
    <div class="form">
      <slot></slot>
    </div>
  </div>
</template>

<style>
.login {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.bg-box {
  overflow: hidden;
  position: relative;
  border: 1px solid #c4edde;
}
.rotate-box {
  position: absolute;
  left: -120px;
  top: -120px;
  width: 600px;
  height: 600px;
  background: linear-gradient(to left, #c4edde, #7ac7c4, #f73859, #384259 80%);
  animation: Rotating 2s linear infinite;
}
@keyframes Rotating {
  100% {
    transform: rotate(360deg);
  }
}
</style>

<script setup lang="ts">
// import { defineComponent } from 'vue'
defineProps({
  style: {
    type: Object as () => Record<string, string>, // 使用 Record<string, string> 类型来传递样式
    required: true,
  },
})
</script>
