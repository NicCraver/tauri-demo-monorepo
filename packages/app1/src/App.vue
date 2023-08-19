<script setup lang="ts">
</script>

<template>
  <transition name="width-transition">
    <div class="home">
      <!-- 配合css 和 tauri约定的属性 实现拖拽功能 -->
      <div class="drag-region" data-tauri-drag-region />
      <div class="left">
        <img src="../src-tauri/icons/icon.png" alt="">
      </div>
      <div class="right">
        Tauri
      </div>
    </div>
  </transition>
</template>

<style scoped>
.home {
  width: 130px;
  height: 38px;
  line-height: 38px;
  border-radius: 8px;
  background-color: #fff;
  color: #000;
  overflow: hidden;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  transition: width 0.5s ease;
  display: flex;
  justify-content: center;
}

.drag-region {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  width: 50px;
  height: 100%;
}

.left {
  width: 45px;
  background-image: linear-gradient(to right top, #0798FB 0%, #0C53FF 40%, #0C53FF 90%, #0C53FF 100%);
  border-top-left-radius: 8px;
  border-bottom-left-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.left img {
  width: 20px;
  height: 20px;
}

.right {
  flex: 1;
  color: #0C53FF;
  font-size: 16px;
  text-align: center;
  background-image: linear-gradient(to top, #e6e9f0 0%, #E6EDFF 100%);
  border-top-right-radius: 8px;
  border-bottom-right-radius: 8px;
}
</style>
