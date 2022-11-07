<script setup lang="ts">
import TheHeader from "@/components/TheHeader.vue";
import TheFooter from "@/components/TheFooter.vue";
</script>

<template>
  <TheHeader />
  <RouterView class="main" />
  <TheFooter />
</template>

<style lang="scss" scoped>
.main {
  height: calc(100vh - 80px);
}
</style>
