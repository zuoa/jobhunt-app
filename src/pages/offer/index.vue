<template>
  <view class="content">
    <view class="section">
      <view class="section-header">
        <image src="/static/image/ICON_GW_SELECTED.png"></image>
        <text>精选岗位</text>
      </view>

      <view class="section-body">
        <scroll-view scroll-y="true">
          <view class="job-item" v-for="(item,index) in courses " :key="item.id">
            <view class="job-header">
              <text class="job-title">{{ item.title }}</text>
              <text class="job-emolument">{{ item.emolument }}</text>
            </view>
            <view class="job-body">
              <text v-for="tag in item.tags" class="tag">
                {{ tag }}
              </text>
            </view>
            <view class="job-footer">
              <view class="company">
                <text>{{ item.company.name }}</text>
                <text>{{ item.company.industry }}</text>
                <text>{{ item.company.size }}</text>
              </view>
              <view>
                <text>{{ item.location }}</text>
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
          "id": 1,
          "title": "软件工程师",
          "description": "负责公司产品的软件开发和维护工作，要求熟练掌握至少一种编程语言。",
          "emolument": "15000-25000元/月",
          "company": {
            "name": "创新科技有限公司",
            "industry": "信息技术",
            "size": "500-1000人"
          },
          "location": "北京",
          "tags": ["编程", "软件开发", "技术"]
        },
        {
          "id": 2,
          "title": "市场经理",
          "description": "负责市场调研和产品推广策略的制定，要求有良好的市场分析能力和沟通技巧。",
          "emolument": "20000-30000元/月",
          "company": {
            "name": "环球市场顾问公司",
            "industry": "市场咨询",
            "size": "100-500人"
          },
          "location": "上海",
          "tags": ["市场", "营销", "管理"]
        },
        {
          "id": 3,
          "title": "财务分析师",
          "description": "负责公司的财务分析和预算编制，要求有会计或财务相关背景。",
          "emolument": "10000-18000元/月",
          "company": {
            "name": "财智财务服务集团",
            "industry": "金融服务",
            "size": "50-100人"
          },
          "location": "广州",
          "tags": ["财务", "分析", "预算"]
        },
        {
          "id": 4,
          "title": "人力资源专员",
          "description": "负责员工招聘、培训和绩效评估等工作，要求有人力资源管理经验。",
          "emolument": "8000-15000元/月",
          "company": {
            "name": "人才发展中心",
            "industry": "人力资源",
            "size": "20-50人"
          },
          "location": "深圳",
          "tags": ["人力资源", "招聘", "培训"]
        },
        {
          "id": 5,
          "title": "客户服务代表",
          "description": "负责解答客户的咨询和处理客户投诉，要求有良好的服务意识和沟通能力。",
          "emolument": "6000-10000元/月",
          "company": {
            "name": "客户关怀服务公司",
            "industry": "客户服务",
            "size": "100-500人"
          },
          "location": "杭州",
          "tags": ["客服", "服务", "沟通"]
        },
        {
          "id": 6,
          "title": "项目经理",
          "description": "负责项目的规划、执行和监控，要求有项目管理经验和领导能力。",
          "emolument": "25000-35000元/月",
          "company": {
            "name": "项目管理解决方案公司",
            "industry": "项目管理",
            "size": "50-100人"
          },
          "location": "成都",
          "tags": ["项目管理", "领导", "规划"]
        },
        {
          "id": 7,
          "title": "数据分析师",
          "description": "负责收集和分析数据，为业务决策提供数据支持，要求熟练使用数据分析工具。",
          "emolument": "12000-22000元/月",
          "company": {
            "name": "数据洞察分析公司",
            "industry": "数据分析",
            "size": "20-50人"
          },
          "location": "武汉",
          "tags": ["数据分析", "数据挖掘", "统计"]
        },
        {
          "id": 8,
          "title": "平面设计师",
          "description": "负责公司产品的视觉设计工作，要求有良好的审美和设计能力。",
          "emolument": "8000-15000元/月",
          "company": {
            "name": "创意视觉设计工作室",
            "industry": "设计",
            "size": "10-20人"
          },
          "location": "南京",
          "tags": ["设计", "视觉", "创意"]
        },
        {
          "id": 9,
          "title": "行政助理",
          "description": "负责办公室日常行政事务和文档管理工作，要求有组织能力和细致的工作态度。",
          "emolument": "5000-8000元/月",
          "company": {
            "name": "行政管理服务公司",
            "industry": "行政管理",
            "size": "10-20人"
          },
          "location": "西安",
          "tags": ["行政", "管理", "文档"]
        },
        {
          "id": 10,
          "title": "销售代表",
          "description": "负责产品的销售和客户关系维护，要求有销售经验和良好的人际关系。",
          "emolument": "底薪+提成",
          "company": {
            "name": "领先销售集团",
            "industry": "销售",
            "size": "100-500人"
          },
          "location": "重庆",
          "tags": ["销售", "客户关系", "业绩"]
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
  background-color: #F9F9F9;
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
  background: #F9F9F9;
  margin: 0 16rpx;
}

.job-item {
  background: #FFF;
  display: flex;
  flex-direction: column;
  margin-bottom: 16rpx;
  padding: 32rpx;
  font-size:28rpx;
}

.job-header {
  display: flex;
  justify-content: space-between;
  flex-direction: row;
}

.job-title {
  font-size: 32rpx;
  font-weight: bold;
  color: #333;
}

.job-emolument {
  font-weight: bold;
  font-size: 28rpx;
  color: #cccc33;
}
.job-body{
  margin: 16rpx 0;
}
.post-item image {
  height: 160rpx;
  width: 240rpx;
  border-radius: 12rpx;
}
.job-footer {
  font-size: 24rpx;
  color:#7F7F7F;
  display: flex;
  justify-content: space-between;
  flex-direction: row;
}

.company {
  display: flex;
  flex-direction: row;
}
.company text{
  border-right:1px solid #eee;
  padding:0 8rpx;
}

.company text:last-child{
  border:none
}

.tag {
  background: #f6f6f6;
  color: #7f7f7f;
  border-radius: 8rpx;
  font-size: 24rpx;
  margin-right:16rpx;
  padding:4rpx 12rpx;
}
</style>
