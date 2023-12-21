<template>
  <nut-tabbar bottom safe-area-inset-bottom placeholder>
    <nut-tabbar-item v-for="(item, index) in List" :key="index" :tab-title="item.title" :icon="item.icon"> </nut-tabbar-item>
  </nut-tabbar>
</template>

<script>
import { h } from 'vue';
import { Home, Category, Find, Cart, My } from '@nutui/icons-vue-taro';

export default {
  // 只支持 Options API 写法，不支持 <script setup>
  // 该配置可以显示Tabbar图标，不加该配置，图标不显示
  options: {
    addGlobalClass: true,
  },
  setup() {
    const List = [
      {
        title: '首页',
        icon: h(Home)
      },
      {
        title: '标签',
        icon: h(Category)
      },
      {
        title: '标签',
        icon: h(Find)
      },
      {
        title: '标签',
        icon: h(Cart)
      },
      {
        title: '我的',
        icon: h(My)
      }
    ];
    return {
      List
    };
  }
};
</script>

<style lang="scss"></style>
