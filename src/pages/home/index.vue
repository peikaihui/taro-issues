<template>
  <view class="index">
    <text>{{ msg }}</text>
    <button @click="goPage">index</button>
  </view>
</template>

<script>
import { ref } from 'vue'
import './index.scss'
import { reLaunch } from '@tarojs/taro';

export default {
  setup () {
    const msg = ref('Hello home')
    const goPage = ()=> {
      reLaunch({
        url: '/pages/index/index?id=78',
      })
    }
    return {
      msg,
      goPage
    }
  }
}
</script>
