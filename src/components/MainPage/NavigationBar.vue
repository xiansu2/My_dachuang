<template>
  <div class="navbar">
    <!-- Logo -->
    <div class="navbar-logo">Logo</div>
    <!-- 导航菜单 -->
    <div class="navbar-menu">
      <!-- 遍历导航项 -->
      <div class="navbar-item" v-for="(item, index) in navItems" :key="index">
        <!-- 标题 -->
        <span @click="menuVisible[index] = !menuVisible[index]">{{ item.label }}</span>
        <!-- 下拉菜单 -->
        <div class="navbar-dropdown" v-show="menuVisible[index]">
          <!-- 遍历下拉菜单项 -->
          <a v-for="(subItem, subIndex) in item.subItems" :key="subIndex">{{ subItem }}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    // 定义导航项和下拉菜单项
    return {
      navItems: [
        { label: 'Home', subItems: ['News', 'Notice'] },
        { label: 'Test', subItems: ['text-to-video', 'image-to-video'] },
        { label: 'About us', subItems: ['API','Team introduction','call us'] }
      ],
      // 定义下拉菜单是否可见的状态
      menuVisible: [false, false, false]
    };
  }
};
</script>

<style scoped>
.navbar {
  display: flex;
  position: fixed;
  top: 0;
  justify-content: space-between;
  align-items: center;
  background: #333;
  color: #fff;
  height: 60px;
  padding: 0 20px;
  flex-direction: row; /* 将导航栏的排列方式修改为横向 */
}

.navbar-logo {
  font-size: 24px;
  font-weight: bold;
}

.navbar-menu {
  display: flex;
  align-items: center;
}

.navbar-item {
  margin-right: 20px;
  position: relative;
  -webkit-text-size-adjust: auto; /* Safari, Chrome, Opera */
  -ms-text-size-adjust: auto; /* IE */
  text-size-adjust: auto; /* Android, iOS */
}

/* 鼠标悬停时显示下拉菜单 */
.navbar-item:hover .navbar-dropdown {
  display: block;
}

.navbar-dropdown {
  display: none;
  white-space: nowrap;
  position: absolute;
  top:calc(100%+5px);
  left:0;
  background-color: #ffffff;
  border-radius: 4px;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.1);
  padding: 0 10px 0 10px;
  z-index: 1;
}

.navbar-dropdown a {
  display: block;
  width:100%;
  padding: 6px 12px;
  font-size: 14px;
  color: #666666;
  cursor: pointer;
}

.navbar-dropdown a:hover {
  background-color: #c7eb78;
}
</style>
