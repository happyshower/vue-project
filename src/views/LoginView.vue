<template>
  <LinearColorLoginBox>
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
</LinearColorLoginBox>
</template>

<style>
</style>

<script lang="ts" setup>
import router from '@/router'
import { reactive } from 'vue'
import BlockSlideLoginBox from '@/components/BlockSlideLoginBox.vue';
import LinearColorLoginBox from '@/components/LinearColorLoginBox.vue';

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
