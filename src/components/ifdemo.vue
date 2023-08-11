<template>
  <h3>条件渲染</h3>
  <div v-if="flag">你能看见我么</div>
  <div v-else>那你看看我吧</div>
  <div v-if="type === 'A'">A</div>
  <div v-else-if="type === 'B'">B</div>
  <div v-else-if="type === 'C'">C</div>
  <div v-else>D</div>
</template>
<script>
export default {
  data() {
    return {
      flag: false,
      type: "A",
    };
  },
};
</script>
