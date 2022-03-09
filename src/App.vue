<template>
  <a-layout>
<!--    Menu-->
    <Sidebar v-model:collapsed="collapsed"/>
    <a-layout>
<!--    Header-->
    <Navbar/>
<!--    Content-->
    <Content/>
    </a-layout>
  </a-layout>
</template>

<script lang="ts">
import Sidebar from "@/components/layouts/sidebar.vue";
import Navbar from "@/components/layouts/navbar.vue";
import Content from "@/components/layouts/content.vue";
export default {
components:{
  Sidebar,
  Navbar,
  Content
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
}

</style>
