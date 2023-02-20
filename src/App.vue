<script>
export default {
  data() {
    return {
      gorod: "Выберите город",
    };
  },
  methods: {},
};
</script>
<template>
  <select v-model="gorod">
    <option class="button">Симферополь</option>
    <option class="button">Сызрань</option>
    <option class="button">Киев</option>
    <option class="button">Россия</option>
    <option class="button">Крым</option>
    <option class="button">Ривия</option>
  </select>
  &nbsp;
  <p>{{ gorod }}</p>
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