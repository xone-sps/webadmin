<template>
  <a-layout-content>
    <a-row>
      <a-col :span="12">
        <a-card size="small" title="Small size card" style="width: 300px">
          <template #extra><a href="#">more</a></template>
          <p>card content</p>
          <p>card content</p>
          <p>card content</p>
        </a-card>
      </a-col>
      <a-col :span="12">
        <a-card size="small" title="Small size card" style="width: 300px">
          <template #extra><a href="#">more</a></template>
          <p>card content</p>
          <p>card content</p>
          <p>card content</p>
        </a-card>
      </a-col>
    </a-row>
    <br/>
    <a-row>
      <a-col :span="8">
        <a-card title="Default size card" style="width: 300px">
          <template #extra><a href="#">more</a></template>
          <p>card content</p>
          <p>card content</p>
          <p>card content</p>
        </a-card>
      </a-col>
      <a-col :span="8">
        <a-card title="Default size card" style="width: 300px">
          <template #extra><a href="#">more</a></template>
          <p>card content</p>
          <p>card content</p>
          <p>card content</p>
        </a-card>
      </a-col>
      <a-col :span="8">
        <a-card title="Default size card" style="width: 300px">
          <template #extra><a href="#">more</a></template>
          <p>card content</p>
          <p>card content</p>
          <p>card content</p>
        </a-card>
      </a-col>
    </a-row>
  </a-layout-content>
</template>

<script lang="ts">
import {Options, Vue} from 'vue-class-component';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Options({
  components: {
    HelloWorld,
  },
})
export default class Home extends Vue {

}
</script>
