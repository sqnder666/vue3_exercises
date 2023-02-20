<script>
export default {
  data() {
    return {
      checked: true,
    };
  },
  methods: {},
};
</script>
<template>
  <input type="checkbox" v-model="checked" />
  &nbsp;
  <p class="button" v-if="checked">{{ checked }}</p>
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