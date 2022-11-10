<script setup lang="ts">
  // import { computed } from "@vue/reactivity";
  // import { ref } from "vue";

  // const formatDay = computed(() => {
  //   const now = new Date();
  //   const year = now.getFullYear();
  //   const month = now.getMonth() + 1;
  //   const day = now.getDate();
  //   console.log(year + "年" + month + "月" + day + "日");
  //   return `${year}年 ${month}月 ${day}日`;
  // });
</script>

<template>
  <header>
    <div class="head">
      <figure>
        <img src="@/assets/img/icon.svg" alt="" srcset="" />
      </figure>
      <h1 class="left_title">mavs-kintai</h1>
    </div>
    <div class="contents">
      <div class="user">
        <figure>
          <img src="@/assets/img/icon.svg" alt="" srcset="" />
        </figure>
        <p>User Name</p>
      </div>
      <div class="logout">
        <button>ログアウト</button>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  header {
    position: fixed;
    z-index: 999;
    top: 0;
    width: 100%;
    padding: 20px;
    box-shadow: 0px 10px 10px -5px rgba(0, 0, 0, 0.5);
    background-color: $colorPurple;
    @include flex(space-between, center);
    .head {
      @include flex(unset, center);
      column-gap: 8px;
      min-width: 260px;
      &_title {
        font-weight: bold;
        font-size: 1.4rem;
      }
    }
    .contents {
      flex: 1;
      @include flex(end, center);
      gap: 14%;
      .user {
        display: flex;
        justify-content: space-around;
        align-items: center;
      }
      .logout {
        background-color: $colorGray;
        border-radius: 5%;
        padding: 10px;
        &:hover {
          // animation つけたい
          opacity: 0.8;
        }
      }
    }
  }
</style>
