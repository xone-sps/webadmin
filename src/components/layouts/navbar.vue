<template>
  <a-layout>
    <a-layout>
      <a-layout-header style="background: #fff; padding-left: 12px">
        <menu-unfold-outlined
            v-if="collapsed"
            class="trigger"
            @click="toggleCollapse"
        />
        <menu-fold-outlined v-else class="trigger" @click="toggleCollapse"/>
        <!--        Avatar-->

<!--    <a-avatar>-->
<!--      <template #icon>-->
<!--        <UserOutlined />-->
<!--      </template>-->
<!--    </a-avatar>-->

<!--        <a-row>-->
<!--          <a-col>-->
<!--                    <a-avatar style="margin-left: 80px">-->
<!--                      <template #icon>-->
<!--                        <UserOutlined />-->
<!--                      </template>-->
<!--                    </a-avatar>-->
<!--          </a-col>-->
<!--        </a-row>-->

      </a-layout-header>
    </a-layout>
  </a-layout>
</template>
<script lang="ts">
import {
  MenuUnfoldOutlined,
  MenuFoldOutlined,
  UserOutlined
} from '@ant-design/icons-vue';
import {defineComponent, ref} from 'vue';

export default defineComponent({
  components: {
    MenuUnfoldOutlined,
    MenuFoldOutlined,
    UserOutlined
  },
  props: ["collapsed"],
  setup(props, {emit}) {
    const toggleCollapse = () => {
      emit("update:collapsed", !props.collapsed);
    };
    return {toggleCollapse};
  },
});
</script>
<style>
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
