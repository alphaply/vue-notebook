<script setup>
import ifdemo from "./components/ifdemo.vue";
import fordemo from "./components/fordemo.vue";
import eventdemo1 from "./components/eventdemo1.vue";
</script>
<script>
export default {
  data() {
    return {
      msg: "active",
      hello: "hello",
      num: 1,
      html: "<a href='http://blog.a152.top'>测试</a>",
      objectAttrs: {
        class: "active",
        id: "hello",
      },
    };
  },
};
</script>

<template>
  <div v-bind:class="msg" :id="hello">
    <h3>模板语法</h3>
    <p>{{ num + 5 }}</p>
    <p v-html="html"></p>
  </div>
  <div v-bind="objectAttrs">测试绑定多个</div>
  <hr />
  <ifdemo />
  <hr />
  <fordemo />
  <hr />
  <eventdemo1 />
</template>

<style>
.active {
  color: blue;
}
</style>
