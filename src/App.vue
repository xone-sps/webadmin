<template>
  <a-layout>
    <!--    Menu-->
    <Sidebar v-model:collapsed="collapsed"
    />
    <a-layout>
      <!--    Header-->
      <Navbar v-model:collapsed="collapsed"/>
      <!--    Content-->
      <Content/>
    </a-layout>
  </a-layout>
</template>

<script lang="ts">
import {defineComponent, ref} from 'vue';
import Sidebar from "@/components/layouts/sidebar.vue";
import Navbar from "@/components/layouts/navbar.vue";
import Content from "@/components/layouts/content.vue";

export default defineComponent({
  components: {
    Sidebar,
    Navbar,
    Content
  },
  setup() {
    return {
      collapsed: ref<boolean>(false),
    }
  }
});
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
