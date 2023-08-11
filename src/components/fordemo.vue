<template>
  <h3>列表渲染</h3>
  <p v-for="item in names">{{ item }}</p>

  <div v-for="i in r">
    <p>{{ i.name }}</p>
    <img :src="i.age" />
  </div>
  <hr />
  <div>
    <p v-for="(value, key, index) in userInfo">
      {{ value }}-{{ key }}-{{ index }}
      <hr>
    </p>
<hr>
<h3>key属性添加到元素属性</h3>
<p v-for="(item,index) in names" :key="index">{{ item }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      names: ["a", "b", "c"],

      r: [
        { id: 1, name: "a", age: 10 },
        { id: 2, name: "b", age: 12 },
        { id: 3, name: "c", age: 13 },
      ],

      userInfo: {
        name: "alpha",
        age: 18,
        sex: "男"
      },
    };
  },
};
</script>
