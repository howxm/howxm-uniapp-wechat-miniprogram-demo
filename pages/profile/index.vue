<template>
  <view class="content">
    <view class="text-area">
      <text class="title">{{ title }}</text>
    </view>
    <button @click="handleClick">Event</button>
    <navigator url="/pages/index/index">转向到首页</navigator>
    <howxm-widget path="/pages/profile/index"/>

  </view>
</template>

<script>
const howxm = requirePlugin('howxm-plugin') //引入浩客sdk

export default {
  data() {
    return {
      title: '信息页',
    }
  },
  onLoad() {
  },
  methods: {
    handleClick() {
      howxm.event('show')
    },
  }
}
</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200 rpx;
  width: 200 rpx;
  margin-top: 200 rpx;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 50 rpx;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36 rpx;
  color: #8f8f94;
}
</style>
