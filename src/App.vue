<script>
export default {
  data() {
    return {
      choice: "",
      english: true,
      russian: false,
      malagas: false,
    };
  },
  methods: {
    eng: function () {
      this.english = true;
      this.russian = false;
      this.malagas = false;
    },
    rus: function () {
      this.english = false;
      this.russian = true;
      this.malagas = false;
    },
    mal: function () {
      this.english = false;
      this.russian = false;
      this.malagas = true;
    },
  },
};
</script>
<template>
  <p class="button" v-if="english">What is your mother tongue?</p>
  <p class="button" v-if="russian">Какой ваш родной язык?</p>
  <p class="button" v-if="malagas">Inona ny fitenin-drazanao?</p>
  &nbsp;
  <input
    class="button"
    name="radio"
    type="radio"
    v-model="choice"
    value="English"
    @click="eng"
  />
  &nbsp;
  <input
    class="button"
    name="radio"
    type="radio"
    v-model="choice"
    value="Русский"
    @click="rus"
  />
  &nbsp;
  <input
    class="button"
    name="radio"
    type="radio"
    v-model="choice"
    value="Малагасийский"
    @click="mal"
  />
  &nbsp;
  <p class="button">{{ choice }}</p>
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