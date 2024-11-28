<template>
  <div class="login">
    <div class="bg-box">
      <div class="rotate-box"></div>
    </div>
    <div class="form">
      <el-form :model="form" label-width="auto" style="max-width: 600px">
        <el-form-item label="Name">
          <el-input v-model="form.name" />
        </el-form-item>
        <el-form-item label="Password">
          <el-input type="password" v-model="form.password" show-password style="width: 200px" />
        </el-form-item>
        <el-form-item>
          <el-button type="primary" @click="onSubmit">Submit</el-button>
          <el-button>Cancel</el-button>
        </el-form-item>
      </el-form>
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
  height: 300px;
  width: 300px;
  background: white;
  position: absolute;
}
.bg-box {
  overflow: hidden;
  width: 310px;
  height: 310px;
  position: relative;
  border: 1px solid #c4edde;
  /* border: 1px solid #f73859; */
  /* box-shadow: -3px -3px #384259,
              3px 3px #384259; */
}
.rotate-box {
  position: absolute;
  /* top: -100px;
  left: -100px; */
  margin-left: 155px;
  margin-top: 155px;
  width: 600px;
  height: 50px;
  transform-origin: 0px 0px;
  background: linear-gradient(to left, #c4edde, #7ac7c4, #f73859, #384259 80%);
  animation: Rotating 2s linear infinite;
}
@keyframes Rotating {
  100% {
    transform: rotate(360deg);
  }
}
</style>

<script lang="ts" setup>
import router from '@/router'
import { reactive } from 'vue'

// do not use same name with ref
const form = reactive({
  name: '',
  password: '',
})

const onSubmit = () => {
  if (form.name === 'admin' && form.password === '123456') {
    router.push('home')
  } else {
    alert('What Happen???')
  }
}
</script>
