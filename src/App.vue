<script>
export default {
  data() {
    return {
      value: ["1", "2", "3", "4", "5"],
    };
  },
  methods: {
    removeItem: function (index) {
      this.value.splice(index, 1);
    },
  },
};
</script>
<template>
  <ul>
    <li v-for="(item, index) in value" :key="index">
      <button class="button" @click="removeItem(index)">{{ item }}</button>
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