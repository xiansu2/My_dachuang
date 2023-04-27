<!--这里面的是要渲染的内容-->
<template>
  <div id="app">
    <header>
      <Navbar />
    </header>
  </div>
</template>

<!--引用导入-->
<script>
import Navbar from './components/Main/NavigationBar.vue';

export default{
  components:{
    Navbar
  }
};
</script>

