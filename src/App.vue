<script setup lang="ts">
import TheHeader from "@/components/TheHeader.vue";
import TheHeaderSp from "@/components/sp/TheHeaderSp.vue";
import TheSidebar from "@/components/TheSidebar.vue";
</script>

<template>
  <TheHeader class="onlyPC" />
  <TheHeaderSp class="onlySP" />
  <main>
    <!-- <TheSidebar class="side" /> -->
    <RouterView class="contents" />
  </main>
</template>

<style lang="scss" scoped>
main {
  display: flex;

  .contents {
    height: calc(100vh - 80px);
    margin: 0 140px;
    flex: 1;
    padding-top: 40px;
  }
}
</style>
