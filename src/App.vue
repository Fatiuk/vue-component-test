<script setup>
import { RouterView } from 'vue-router'
import PageHeader from './components/PageHeader.vue'
</script>

<template>
  <div>
    <PageHeader />
    <RouterView />
  </div>
</template>
