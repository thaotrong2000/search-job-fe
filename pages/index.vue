<template>
  <a-layout id="components-layout-demo-side" style="min-height: 100vh">
    <a-layout-sider v-model="collapsed" collapsible>
      <div class="logo" />
      <a-menu theme="dark" :default-selected-keys="['1']" mode="inline">
        <a-menu-item key="1">
          <nuxt-link to="/all-job" class="!flex items-center">
            <a-icon type="pie-chart" />
            <span>All jobs</span>
          </nuxt-link>
        </a-menu-item>
        <a-menu-item key="2">
          <nuxt-link to="/companies" class="!flex items-center">
            <a-icon type="desktop" />
            <span>IT Companies</span>
          </nuxt-link>
        </a-menu-item>
      </a-menu>
    </a-layout-sider>
    <a-layout>
      <a-layout-header class="flex !bg-white !px-4 !py-1">
        <div class="user-infor flex items-center ml-auto">
          <span class="username mr-1">UET-IT</span>
          <a-icon type="caret-down" />
        </div>
      </a-layout-header>
      <a-layout-content style="margin: 0 16px">
        <nuxt-child />
      </a-layout-content>
      <a-layout-footer style="text-align: center">
        Team23 ©2023 Created by Team23
      </a-layout-footer>
    </a-layout>
  </a-layout>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      collapsed: false,
    }
  }
}
</script>
