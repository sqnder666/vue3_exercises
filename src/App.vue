<script>
export default {
  data() {
    return {
      languages: [],
    };
  },
  methods: {},
};
</script>
<template>
  <input class="button" type="checkbox" v-model="languages" value="никакой" />
  <p>никакой</p>
  <input class="button" type="checkbox" v-model="languages" value="русский" />
  <p>русский</p>
  <input class="button" type="checkbox" v-model="languages" value="армянский" />
  <p>армянский</p>
  <ul v-for="elem in languages">
    <li>{{ elem }}</li>
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