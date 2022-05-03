<template>
  <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" menu-trigger="click" @select="handleSelect">
    <el-menu-item index="1">Processing Center</el-menu-item>
    <el-submenu index="2">
      <template slot="title">Workspace</template>
      <el-menu-item index="2-1">item one</el-menu-item>
      <el-menu-item index="2-2">item two</el-menu-item>
      <el-menu-item index="2-3">item three</el-menu-item>
      <el-submenu :popper-append-to-body="false" index="2-44">
        <template slot="title">item four</template>
        <el-menu-item index="2-4-14">sub item 1</el-menu-item>
        <el-menu-item index="2-4-24">sub item 2</el-menu-item>
        <el-menu-item index="2-4-34">sub item 3</el-menu-item>
        <el-submenu :popper-append-to-body="false" index="2-414">
          <template slot="title">item four</template>
          <el-menu-item index="2-4-124">sub item 1</el-menu-item>
          <el-menu-item index="2-4-2334">sub item 2</el-menu-item>
          <el-menu-item index="2-4-344">sub item 3</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-submenu :popper-append-to-body="false" index="2-4">
        <template slot="title">item four</template>
        <el-menu-item index="2-4-1">sub item 1</el-menu-item>
        <el-menu-item index="2-4-2">sub item 2</el-menu-item>
        <el-menu-item index="2-4-3">sub item 3</el-menu-item>
        <el-submenu :popper-append-to-body="false" index="2-41">
          <template slot="title">item four</template>
          <el-menu-item index="2-4-12">sub item 1</el-menu-item>
          <el-menu-item index="2-4-233">sub item 2</el-menu-item>
          <el-menu-item index="2-4-34">sub item 3</el-menu-item>
        </el-submenu>
      </el-submenu>
    </el-submenu>
    <el-menu-item index="3" disabled>Info</el-menu-item>
    <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">Orders</a></el-menu-item>
  </el-menu>
</template>

<script>
  export default {
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>