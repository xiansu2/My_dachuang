<!--用户登录组件-->
<template>
  <form>
  <h2>Login Form</h2>
  <!--用户名称输入-->
  <label for="username">Username:</label>
  <input type="text" id="username">
  <br>  <!--换行符-->
  <!--密码输入-->
  <label for="password">Password:</label>
  <input type="password" id="password">
  <br>
  <!--设置按钮-->
  <button type="submit">Login</button>
  </form>
</template>

<!--使用export default将此组件暴露出去以便使用-->
<script>
export default{
  name='LoginForm'
}
</script>