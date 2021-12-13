<template>
  <view class="index">
    <text>{{ msg }}</text>
    <button @click="goPage">home</button>
  </view>
</template>

<script>
import { ref } from 'vue'
import './index.scss'
import { reLaunch } from '@tarojs/taro';

export default {
  setup () {
    const msg = ref('Hello world')
        const goPage = ()=> {
      reLaunch({
        url: '/pages/home/index',
      })
    }
    return {
      msg,
      goPage,
    }
  }
}
</script>
