<template>
  <div class="home">
    <h2>近期活动</h2>
    <el-table :data="activities" style="width: 100%">
      <el-table-column prop="name" label="活动名称" width="180" />
      <el-table-column prop="date" label="日期" width="120" />
      <el-table-column prop="location" label="地点" />
      <el-table-column label="操作">
        <template #default="scope">
          <el-button size="small" @click="viewDetail(scope.row.id)">详情</el-button>
          <el-button size="small" type="primary" @click="signUp(scope.row.id)">报名</el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activities: [
        { id: 1, name: '校园歌唱比赛', date: '2023-06-15', location: '学校礼堂' },
        { id: 2, name: '编程马拉松', date: '2023-06-20', location: '计算机实验室' }
      ]
    }
  },
  methods: {
    viewDetail(id) {
      this.$router.push(`/activity/${id}`)
    },
    signUp(id) {
      alert(`报名活动ID: ${id}`)
    }
  }
}
</script>

<style scoped>
.home {
  padding: 20px;
}
</style>