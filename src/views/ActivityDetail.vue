<template>
  <div class="detail">
    <h2>{{ activity.name }}</h2>
    <p>日期：{{ activity.date }}</p>
    <p>地点：{{ activity.location }}</p>
    <el-button @click="$router.go(-1)">返回</el-button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activity: {}
    }
  },
  created() {
    // 模拟数据加载
    this.activity = {
      id: this.$route.params.id,
      name: '示例活动',
      date: '2023-06-15',
      location: '学校礼堂'
    }
  }
}
</script>