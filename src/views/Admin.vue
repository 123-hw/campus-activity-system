<template>
  <div class="login">
    <el-form label-width="80px">
      <h2>用户登录</h2>
      <el-form-item label="账号">
        <el-input v-model="form.username" />
      </el-form-item>
      <el-form-item label="密码">
        <el-input v-model="form.password" type="password" />
      </el-form-item>
      <el-button type="primary" @click="handleLogin">登录</el-button>
    </el-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: { username: '', password: '' }
    }
  },
  methods: {
    handleLogin() {
      console.log('登录信息:', this.form)
      this.$router.push('/')
    }
  }
}
</script>

<style scoped>
.login {
  width: 400px;
  margin: 100px auto;
}
</style>