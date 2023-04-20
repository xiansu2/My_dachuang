<template>
  <!-- 显示登录表单 -->
  <form>
    <h2>Login Form</h2>
    <!-- 用户名输入框 -->
    <label for="username">Username:</label>
    <input type="text" id="username" />
    <br />
    <!-- 密码输入框 -->
    <label for="password">Password:</label>
    <input type="password" id="password" />
    <br />
    <!-- 登录按钮 -->
    <button type="submit">Login</button>
  </form>
</template>

<script>
export default {
  name: 'LoginForm', // 定义组件名称
};
</script>
