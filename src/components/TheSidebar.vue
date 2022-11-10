<script setup lang="ts">
  // import { Ref, ref } from "vue";

  import { ref } from "vue";

  // const isOpenSubMenu: Ref<boolean> = ref(true);

  // const toggleSubMenu = () => {
  //   isOpenSubMenu.value = !isOpenSubMenu.value;
  // };
  const menu = ref(["ホーム", "マイページ", "申請"]);
</script>

<template>
  <div class="side">
    <ul class="menu">
      <li v-for="i in menu" :key="i" class="menu_item">
        <figure>
          <img src="@/assets/img/icon.svg" alt="" srcset="" />
        </figure>
        <p>{{ i }}</p>
      </li>
    </ul>
    <ul class="subMenu">
      <li v-for="i in 4" :key="i" class="subMenu_item">サブメニュ</li>
      <img class="toggle" src="@/assets/img/icon.svg" alt="" srcset="" />
    </ul>
  </div>
</template>

<style lang="scss" scoped>
  .side {
    width: 280px;
    @include mq(sp) {
      width: 20px;
      font-size: 4rem;
    }

    background-color: $colorLightBlack;
    display: flex;
    .menu {
      background-color: $colorPurple;
      width: 80px;
      &_item {
        cursor: pointer;
        &:first-child {
          background-color: $colorLightPurple;
          padding-top: 10px;
        }
        &:hover {
          background-color: $colorLightPurple;
        }
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        padding: 8px;
        figure {
          padding: 8px;
          img {
            width: 100%;
          }
        }
        p {
          font-size: 0.8rem;
          font-weight: bold;
        }
      }
    }
    .subMenu {
      position: relative;
      background-color: $colorLightPurple;
      opacity: 0.8;
      flex: 1;
      padding: 24px;
      &_item {
        padding: 10px;
        cursor: pointer;
        border-bottom: 1px solid $colorGray;
        &:hover {
          background-color: $colorSubMenuHover;
        }
        &:first-child {
          margin-top: 20px;
          background-color: $colorSubMenuHover;
        }
      }
      .toggle {
        position: absolute;
        top: 6px;
        right: 6px;
      }
    }
  }
</style>
