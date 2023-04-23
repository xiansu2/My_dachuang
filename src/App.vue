<template>
  <div class="countainer">
    <!--渲染LoginForm和RegisterForm组件-->
    <LoginForm></LoginForm>
    <RegisterForm></RegisterForm>
  </div>
</template>

<!--导入-->
<script>
import LoginForm from './components/LoginForm.vue'
import RegisterForm from './components/RegisterForm.vue'

export default{
  name:'LoginPage',
  components:{  //注册组件
    LoginForm,
    RegisterForm
  }
}
</script>

<!--设置style-->
<style scoped>
.container{
  background-color:dodgerblue;
  display:flex;
  justify-content:space-around;
  margin-top:20px;
}
</style>

