<template>
  <view class="content">
    <image class="banner" mode="aspectFill" src="http://iph.href.lu/879x200?fg=666666&bg=cccccc"></image>
    <view class="description-box">
      <rich-text :nodes="description"></rich-text>
    </view>

    <button type="primary" size="large" plain>定制专属VIP服务</button>

    <view class="teacher-box">
      <view class="box">
        <text class="box-title">推荐导师</text>
      </view>
      <scroll-view scroll-x="true" class="scroll-view_H">
        <view id="demo1" class="scroll-view-item_H uni-bg-red">
          <image class="avatar" src="/static/image/bb1.jpg"></image>
          <view>
            <text class="person-name">张大有</text>
          </view>
          <view>
            <text class="person-title">字节跳动资深HR</text>
          </view>
        </view>
        <view id="demo1" class="scroll-view-item_H uni-bg-red">
          <image class="avatar" src="/static/image/bb1.jpg"></image>
          <view>
            <text class="person-name">张大有</text>
          </view>
          <view>
            <text class="person-title">字节跳动资深HR</text>
          </view>
        </view>
        <view id="demo1" class="scroll-view-item_H uni-bg-red">
          <image class="avatar" src="/static/image/bb1.jpg"></image>
          <view>
            <text class="person-name">张大有</text>
          </view>
          <view>
            <text class="person-title">字节跳动资深HR</text>
          </view>
        </view>
        <view id="demo1" class="scroll-view-item_H uni-bg-red">
          <image class="avatar" src="/static/image/bb1.jpg"></image>
          <view>
            <text class="person-name">张大有</text>
          </view>
          <view>
            <text class="person-title">字节跳动资深HR</text>
          </view>
        </view>
      </scroll-view>

    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: 'Hello',
      description: '<div class="title"><h2>你为什么需要一份好的简历</h2><br>企业HR平均每天查看上千份简历<br> 平均每份简历只看6秒钟<br>只有一份规范、专业的简历才能引起HR的注意</div>'
    }
  },
  onLoad() {

  },
  methods: {}
}
</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.banner {
  height: 280rpx;
  width: 100%;

}
.box {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.box-title {
  font-size: 36rpx;
  color: #333;
  font-weight: bold;
  margin: 16rpx 0;
  text-align: center;
  border-bottom: 3px solid #393;
}

.description-box {
  text-align: center;
  margin: 32rpx 0;
}

.scroll-Y {
  height: 300rpx;
}


.teacher-box {
  margin: 32rpx 0;
}

.scroll-view_H {
  white-space: nowrap;
  width: 100%;
}

.scroll-view-item {
  height: 300rpx;
  line-height: 300rpx;
  text-align: center;
  font-size: 36rpx;
}

.scroll-view-item_H {
  display: inline-block;
  width: 33%;
  text-align: center;
  font-size: 36rpx;
}

.avatar {
  width: 160rpx;
  height: 160rpx;
  border-radius: 50%;
  margin: 16rpx auto;
}

.person-name {
  font-size: 48rpx;
  color: #333;
  font-weight: bold;
}

.person-title {
  font-size: 24rpx;
  color: #999;
}
</style>
