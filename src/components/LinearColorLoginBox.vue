<template>
  <div class="login">
    <div class="bg-box" :style="{ width: style.width + 'px', height: style.height + 'px' }">
      <div
        class="rotate-box"
        :style="{ width: style.width + 10 + 'px', height: style.height + 10 + 'px' }"
      ></div>
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
.form {
  display: flex;
  justify-content: center;
  align-items: center;
  /* height: 300px;
  width: 300px; */
  background: white;
  position: absolute;
}
.bg-box {
  overflow: hidden;
  /* width: 310px;
  height: 310px; */
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
var { style } = defineProps(['style'])
</script>
