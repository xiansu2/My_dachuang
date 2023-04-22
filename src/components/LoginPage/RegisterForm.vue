<!--用户注册组件-->
<template>
  <form>
  <h2>Register Form</h2>
  <!--用户名称输入-->
  <label for="username">Username:</label>
  <input type="text" id="username">
  <br>
  <!--用户邮箱输入-->
  <label for="email">Email:</label>
  <input type="email" id="email">
  <br>
  <!--用户密码输入-->
  <label for="password">Password:</label>
  <input type="password" id="password">
  <!--按钮注册-->
  <br>
  <button type="submit">Register</button>
  </form>
</template>

<!--暴露-->
<script>
export default{
  name:'RegisterForm'
}
</script>