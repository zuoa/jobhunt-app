<template>
  <view class="content">

    <view class="container">
      <scroll-view scroll-y="true" class="scroll-box">

        <view v-for="(item,index) in resumeInfo.sections "
              :key="item.id">
          <view v-if="item.type === '基础信息'" class="section basic-info">
            <view class="section-title">
              <text class="section-title-text">{{ item.title }}</text>
              <image class="section-title-edit" src="/static/image/icon_edit.png"></image>
            </view>
            <view class="section-body">

              <view>男</view>
              <view>13999999999</view>
              <view>ccccsdf@dcasdcsd.com</view>
            </view>
          </view>

          <view v-else-if="item.type === '求职意向'" class="section">
            <view class="section-title">
              <text class="section-title-text">{{ item.title }}</text>
              <image class="section-title-edit" src="/static/image/icon_edit.png"></image>
            </view>
            <view class="section-body">
              {{ item.value }}
            </view>
          </view>
          <view v-else-if="item.type === '个人优势'" class="section">
            <view class="section-title">
              <text class="section-title-text">{{ item.title }}</text>
              <image class="section-title-edit" src="/static/image/icon_edit.png"></image>
            </view>
            <view class="section-body">
              {{ item.value }}
            </view>
          </view>
          <view v-else-if="item.type === '项目经历'" class="section">
            <view class="section-title">
              <text class="section-title-text">{{ item.title }}</text>
              <image class="section-title-edit" src="/static/image/icon_edit.png"></image>
            </view>
            <view class="section-body">
              <view  v-for="(sub_item,index) in item.value "
                     :key="sub_item.id" class="section-item">
                <view class="item-title">
                  <text>{{ sub_item.title }}</text>
                  <image class="more" src="/static/image/icon_more.png"></image>
                </view>
                <view>{{ sub_item.role }}</view>
                <view>{{ sub_item.beginTime }} - {{ sub_item.endTime }}</view>
                <view>{{ sub_item.content }}</view>
                <view>{{ sub_item.performance }}</view>
              </view>
            </view>
          </view>
          <view v-else class="section">
            <view class="section-title">
              <text class="section-title-text">{{ item.title }}</text>
              <image class="section-title-edit" src="/static/image/icon_edit.png"></image>
            </view>
            <view class="section-body">
              {{ item.value }}
            </view>
          </view>
        </view>

      </scroll-view>
    </view>


    <view class="footer">
      <view class="button-group">
        <view class="button button-outline">互联网</view>
        <view class="button button-outline">中文</view>
        <view class="button fill">一键分析</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: 'Hello',
      resumeInfo: {
        sections: [
          {
            id: 1,
            title: '基础信息',
            type: '基础信息',
            fields: [
              {
                label: '姓名',
                value: '张三'
              },
              {
                label: '性别',
                value: '男'
              },
              {
                label: '年龄',
                value: '25'
              },
              {
                label: '电话',
                value: '13999999999'
              },
              {
                label: '邮箱',
                value: ''
              }

            ],
          },
          {
            id: 2,
            title: '求职意向',
            type: '求职意向',
            value: '前端开发工程师',
          },
          {
            id: 3,
            title: '个人优势',
            type: '个人优势',
            value: '前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师',
          },
          {
            id: 4,
            title: '项目经历',
            type: '项目经历',
            value:[
              {
                id: 1,
                title: '项目名称',
                role: '前端开发工程师',
                beginTime: '2019.01',
                endTime: '至今',
                content: '项目描述',
                performance: '项目业绩'
              },
              {
                id: 2,
                title: '项目名称',
                role: '前端开发工程师',
                beginTime: '2019-01',
                endTime: '2019-12',
                content: '项目描述',
                performance: '项目业绩'
              },
              {
                id: 3,
                title: '项目名称',
                role: '前端开发工程师',
                beginTime: '2019-01',
                endTime: '2019-12',
                content: '项目���述',
                performance: '项目业绩'
              },
              {
                id: 4,
                title: '项目名称',
                role: '前端开发工程师',
                beginTime: '2019-01',
                endTime: '2019-12',
                content: '项目描述',
                performance: '项目业绩'
              },
              {
                id: 5,
                title: '项目名称',
                role: '前端开发工程师',
                beginTime: '2019-01',
                endTime: '2019-12',
                content: '项目描述',
                performance: '项目业绩'
              },
              {
                id: 6,
                title: '项目名称',
                role: '前端开发工程师',
                beginTime: '2019-01',
                endTime: '2019-12',
                content: '项目描述',
                performance: '项目业绩'
              },
              {
                id: 7,
                title: '项目名称',
                role: '前端开发工程师',
                beginTime: '2019-01',
                endTime: '2019-12',
                content: '项目描述',
                performance: '项目业绩'
              },
            ]
          },
          {
            id: 5,
            title: '实习经历',
            type: '实习经历',
            value: '前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师',
          },
          {
            id: 6,
            title: '教育经历',
            type: '教育经历',
            value: '前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师前端开发工程师',
          },
        ]
      }
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
  height: 100vh;
  background: #F9F9F9;
}

.fill {
  flex: 1;
}

.container {
  height: 300rpx;
}

.scroll-box {
  height: 90vh;
}

.footer {
  width: 100%;
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100rpx;
  background: #FFF;
  padding-top: 16rpx;
}

.button-group {
  margin: 0 2%;
  width: 96%;
  display: flex;
  flex-direction: row;
}

.button {
  line-height: 48rpx;
  height: 48rpx;
  text-align: center;
  background: #36ab60;
  color: #FFF;
  font-size: 28rpx;
  border-radius: 32rpx;
  padding: 8rpx 32rpx;
  margin: 8rpx;
}

.button-outline {
  background: #FFF;
  color: #36ab60;
  border: 1px solid #36ab60;
}

.button-large {
  flex: 1;
  width: 200rpx;
}


.section {
  margin: 16rpx;
  border-radius: 16rpx;
  background: #FFF;
  padding: 8rpx;
  box-shadow: 0 5rpx 15rpx #eee;
  border: 1px solid #eee;
}

.section-title {
  padding: 8rpx;
  display: flex;
  border-bottom: 1px solid #F3F3F3;
}

.section-title-text {
  flex: 1;
  font-size: 32rpx;
  font-weight: bold;
}

.section-title-edit {
  height: 32rpx;
  width: 32rpx;
}

.section-body {
  padding: 8rpx;
  color: #7F7F7F;
  font-size: 28rpx;
}

.section-item {
  padding: 8rpx;
  font-size: 24rpx;
  border-bottom: 1px dashed #EEE;
}

.item-title {
  padding: 4rpx 0;
  font-size: 28rpx;
  color:#000;
  font-weight: bold;
  display: flex;
  justify-content: space-between;

}

.more {
  width:32rpx;
  height: 32rpx;
}
</style>
