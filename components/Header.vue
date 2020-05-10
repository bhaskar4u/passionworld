<template>
  <div class="container">
    <a-layout id="components-layout-demo-top-side">
      <a-layout-header class="header">
        <div class="logo">
          <h2>Passion World</h2>
        </div>
        <a-menu
          class="menu"
          theme="dark"
          mode="horizontal"
          :default-selected-keys="['2']"
          :style="{ lineHeight: '64px' }"
        >
          <a-menu-item>
            <a href="/">Home</a>
          </a-menu-item>
          <a-menu-item>
            <a href="/member">Member</a>
          </a-menu-item>
        </a-menu>
      </a-layout-header>
    </a-layout>
  </div>
</template>

<style>
#components-layout-demo-top-side .logo {
  width: 150px;
  height: 80px;
  background: rgba(255, 255, 255, 0.103);
  margin: 16px 28px 16px 0;
  float: left;
}
.logo h2 {
  color: white;
  margin-bottom: 20px;
  padding: 5px;
}
.menu {
  float: right;
}
</style>
