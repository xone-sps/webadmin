<template>
  <a-layout-sider v-model:collapsed="collapsed" :trigger="null" collapsible>
    <div class="logo" @click="toggleCollapse">
      <a>Logo</a>
    </div>
    <!--      <a-image :width="40" src="../../assets/logo.png" @click="toggleCollapse"/>-->
    <!--      <a-button @click="toggleCollapse">Logo</a-button>-->

<!--    <div class="logo">-->
<!--      <img :width="30" src="@/assets/logo.png" alt="logo" />-->
<!--      <a>HAL Tech</a>-->
<!--    </div>-->
    <a-menu v-model:selectedKeys="selectedKeys" theme="dark" mode="inline">
      <a-menu-item key="1">
        <video-camera-outlined/>
        <span>nav 2</span>
      </a-menu-item>
      <a-menu-item key="2">
        <upload-outlined/>
        <span>nav 3</span>
      </a-menu-item>

      <a-sub-menu key="sub1">
        <template #title>
            <span>
              <user-outlined/>
              <span>User</span>
            </span>
        </template>
        <a-menu-item key="3">Tom</a-menu-item>
        <a-menu-item key="4">Bill</a-menu-item>
        <a-menu-item key="5">Alex</a-menu-item>
      </a-sub-menu>

    </a-menu>
  </a-layout-sider>
</template>
<script lang="ts">
import {
  UserOutlined,
  VideoCameraOutlined,
  UploadOutlined,
} from '@ant-design/icons-vue';
import {defineComponent, ref} from 'vue';

export default defineComponent({
  components: {
    UserOutlined,
    VideoCameraOutlined,
    UploadOutlined,
  },
  props: ["collapsed"],
  setup(props, {emit}) {
    const toggleCollapse = () => {
      emit("update:collapsed", !props.collapsed);
    }
    return {
      selectedKeys: ref<string[]>(['1']),
      toggleCollapse
    };
  },
});
</script>
<style>

.logo {
  height: 32px;
  margin: 16px;
  background: rgba(255, 255, 255, 0.3);
}

#components-layout-demo-custom-trigger .trigger {
  font-size: 18px;
  line-height: 64px;
  padding: 0 24px;
  cursor: pointer;
  transition: color 0.3s;
}

#components-layout-demo-custom-trigger .trigger:hover {
  color: #1890ff;
}

#components-layout-demo-custom-trigger .logo {
  height: 32px;
  background: rgba(255, 255, 255, 0.3);
  margin: 16px;
}

.site-layout .site-layout-background {
  background: #fff;
}
</style>
