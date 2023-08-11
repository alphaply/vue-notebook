<template>
  <h3>事件处理</h3>
  <button @click="count++">Add</button>
  <p>{{ count }}</p>
  <hr />
  <button @click="addCount(), log($event)">Add 使用事件</button>
  <p>{{ count }}</p>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },

  methods: {
    addCount() {
      this.count += 1;
    },
    log(event) {
      alert(event);
    },
  },
};
</script>
