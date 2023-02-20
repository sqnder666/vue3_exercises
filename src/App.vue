<script>
export default {
  data() {
    return {
      newItem: "",
      items: ["1", "2", "3", "4", "5"],
    };
  },
  methods: {
    addItemEnd: function () {
      this.items.push(this.newItem);
    },
    addItemBegin: function () {
      this.items.unshift(this.newItem);
    },
  },
};
</script>
<template>
  <input v-model="newItem" />
  <button class="button" @click="addItemEnd">maybe im alone</button>
  <button class="button" @click="addItemBegin">or not</button>
  <ul v-for="(item, index) in items" :key="index">
    <li>
      {{ item }}
    </li>
  </ul>
</template>
<style>
.button {
    background-color: #293133; 
    border-radius: 8px;
    border: none;
    color: rgb(255, 255, 255);
    padding: 10px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 15px;
    margin: 4px 2px;
    cursor: pointer;
    -webkit-transition-duration: 0.4s; 
    transition-duration: 0.4s;
}
</style>