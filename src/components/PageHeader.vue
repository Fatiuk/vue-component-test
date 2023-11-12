<template>
  <el-menu
    :default-active="activeIndex"
    class="el-menu-demo"
    mode="horizontal"
    :ellipsis="false"
    :router="true"
  >
    <el-menu-item>
      <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="28" height="28" />
      <h1>Project</h1>
    </el-menu-item>
    <div class="flex-grow"></div>
    <el-menu-item index="/"> Home </el-menu-item>
    <el-menu-item index="/contacts"> Contacts</el-menu-item>
  </el-menu>
</template>

<script lang="ts" setup>
import { onMounted, ref } from 'vue'
onMounted(() => {
  activeIndex.value = window.location.pathname
})

const activeIndex = ref('1')
</script>

<style>
.flex-grow {
  flex-grow: 1;
}
</style>
