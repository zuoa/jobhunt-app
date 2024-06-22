<template>
  <view class="content">
    <view class="big-button" @click="onClick">
      <view>
        <text class="title" @click="onClick">创建简历</text>
      </view>
      <text class="sub-title">海量专业模版，随意创建个性化简历</text>
    </view>


    <view class="big-button" @click="chooseFile">
      <view>
        <text class="title">导入简历</text>
      </view>
      <text class="sub-title">支持PDF、Word格式简历，90%以上内容识别率，自动排版</text>
    </view>


    <scroll-view scroll-x="true" class="scroll-view_H">

      <view class="resume-box">
        <navigator url="/pages/resume/detail?id=1">
          <view class="resume">
            <image class="img" src="/static/image/img_resume.png"></image>
            <text>未命名asa</text>
          </view>
        </navigator>
      </view>
      <view class="resume-box">
        <navigator url="/pages/resume/detail?id=1">
          <view class="resume">
            <image class="img" src="/static/image/img_resume.png"></image>
          </view>
        </navigator>
      </view>
      <view class="resume-box">
        <navigator url="/pages/resume/detail?id=1">
          <view class="resume">
            <image class="img" src="/static/image/img_resume.png"></image>
          </view>
        </navigator>
      </view>
      <view class="resume-box">
        <navigator url="/pages/resume/detail?id=1">
          <view class="resume">
            <image class="img" src="/static/image/img_resume.png"></image>
          </view>
        </navigator>
      </view>
    </scroll-view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: 'Hello'
    }
  },
  onLoad() {

  },
  methods: {
    onClick: function (e) {
      console.log(11111111111111)
      this.title = "111212"
    },


    chooseFile: function (e) {
      let that = this;
      wx.chooseMessageFile({
        count: 1, //限制选择的文件数量
        type: 'file',//非图片和视频的文件,不选默认为all
        extension: ['xls', 'xlsx'],//此处限制文件类型
        // extension: ['xls', 'xlsx'], //此处限制文件类型
        success(res) {
          const tempFilePaths = res.tempFiles
          console.log('临时路径', tempFilePaths)
          //下面是返回后需要调接口的操作
          // 		uni.uploadFile({
          // 			url: 'https://******/index/Api/upload',
          // 			filePath: tempFilePaths[0].path,
          // 			name: 'file_',

          // 			formData: {

          // 			},
          // 			success: (uploadFileRes) => {
          // 				//接口返回的数据
          // 				console.log(uploadFileRes.data);
          // 				that.$token.toast("上传成功", 2000)
          // 				that.file_name = uploadFileRes.data
          // 			}
          // 		});
        }
      })
    }
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
  height: 200rpx;
  width: 200rpx;
  margin: 200rpx auto 50rpx auto;
}

.big-button {
  color:#FFF;
  width: 90%;
  margin: 16rpx 2%;
  padding: 3%;
  height: 200rpx;
  background: #2775b6;

  border: 1px solid #ddd;
  border-radius: 8rpx;
  box-shadow: 0 0 15rpx #eee;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 48rpx;
  color: #fff;
}

.sub-title {

  font-size: 28rpx;
  color: #EEE;
}

.scroll-view_H {
  white-space: nowrap;
  width: 100%;
}

.resume-box {
  display: inline-block;
  width: 33%;
}

.resume {
  background: #FFFFCC;
  display: flex;
  flex-direction: column;
  height: 300rpx;
  padding: 16rpx;
  border: 1px solid #eee;
  margin: 8rpx;
}

.img {
  width: 64rpx;
  height: 64rpx;
}

</style>
