<template>
  <view class="content">
    <view class="banner">
      <image mode="aspectFill" src="/static/image/banner_top.jpeg"></image>
    </view>
    <view class="section">
      <view class="section-header">
        <image src="/static/image/ICON_KC_SELECTED.png"></image>
        <text>精品课程</text>
      </view>

      <view class="section-body">
        <scroll-view scroll-y="true">
          <view class="post-item" v-for="(item,index) in courses " :key="item.id">
            <image src="/static/image/img_banner.jpeg" mode="aspectFill"></image>
            <view class="post-item-content">
              <view>
                <text class="item-title">{{ item.title }}</text>
                <text class="item-description">{{ item.description }}</text>
              </view>
              <view class="item-line">
                <view class="rd">
                  <image src="/static/image/icon_rd.png"></image>
                  <text>{{ item.heat }}</text>
                </view>
                <view class="button">
                  立即领取
                </view>
              </view>
            </view>
          </view>

        </scroll-view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: 'Hello',
      courses: [
        {
          id: 1,
          title: 'JAVA面试技巧',
          description: '阿达阿达是的阿道夫单方事故第三个十多个当当是',
          heat: 100
        },
        {
          id: 2,
          title: 'Python基础',
          description: '阿达阿达是的阿道夫单方事故第三个十多个当当是',
          heat: 100
        },
        {
          id: 3,
          title: 'Vue.js实战',
          description: '阿达阿达是的阿道夫单方事故第三个十多个当当是',
          heat: 100
        },
        {
          id: 4,
          title: 'React.js实战',
          description: '阿达阿达是的阿道夫单方事故第三个十多个当当是',
          heat: 100
        },
        {
          id: 5,
          title: '微信小程序开发',
          description: '阿达阿达是的阿道夫单方事故第三个十多个当当是',
          heat: 100
        },
        {
          id: 6,
          title: 'Flutter实战',
          description: '阿达阿达是的阿道夫单方事故第三个十多个当当是',
          heat: 100
        }
      ]
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
  height: 100vh;
  background: #F9F9F9;
  flex-direction: column;
}

.section {
  flex: 1;
}

.section-header {
  display: flex;
  align-items: center;
  padding: 20rpx;
  background-color: #f8f8f8;
}

.section-header image {
  width: 40rpx;
  height: 40rpx;
  margin-right: 20rpx;
}

.section-header text {
  font-size: 32rpx;
  font-weight: bold;
}

.section-body {
  flex: 1;
  padding: 20rpx;
  background: #FFF;
  border-radius: 16rpx;
  box-shadow: 0 5rpx 15rpx #eee;
  margin: 0 16rpx;
}

.post-item {
  display: flex;
  flex-direction: row;
  margin: 32rpx 8rpx;
  height: 180rpx;
}

.post-item image {
  height: 160rpx;
  width: 240rpx;
  border-radius: 12rpx;
}

.post-item-content {
  flex: 1;
  margin-left: 16rpx;
  display: flex;
  flex-direction: column;
  font-size: 28rpx;
  color: #999;
  justify-content: space-between;
}

.item-title {
  display: block;
  color: #000;
  font-size: 32rpx;
  font-weight: bold;
}

.item-line {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  text-align: center;
  align-items: center;
}

.rd {
  display: flex;

  flex-direction: row;
  justify-content: center;
}

.rd image {
  width: 32rpx;
  height: 32rpx;
  margin-right: 8rpx;
}
.button {
  line-height: 24rpx;
  height: 36rpx;
  text-align: center;
  background: #36ab60;
  color: #FFF;
  font-size: 28rpx;
  border-radius: 32rpx;
  padding: 8rpx 32rpx;
  margin: 8rpx;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.banner {
  margin:2%;
  border-radius: 32rpx;
  width: 96%;
}
.banner image{
  border-radius: 16rpx;
  width:100%;
}
</style>
