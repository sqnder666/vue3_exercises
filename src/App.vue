<script>
export default {
  data() {
    return {
      number: 1,
      number_square: "task1",
      numero_uno: 0,
      numero_dos: 0,
      sum_number: "task2",
      text_uno: "placeholder",
      text_dos: "placeholder",
      fullName: "",
      userName: "",
      userSurname: "",
      userPatronymic: "",
    };
  },
  methods: {
    square: function () {
      this.number_square = this.number ** 2;
    },
    sum: function () {
      this.sum_number = this.numero_uno + this.numero_dos;
    },
    swap: function () {
      const temp = this.text_uno;
      this.text_uno = this.text_dos;
      this.text_dos = temp;
    },
    split: function () {
      this.userSurname = this.fullName.split(" ")[0];
      this.userName = this.fullName.split(" ")[1];
      this.userPatronymic = this.fullName.split(" ")[2];
    },
  },
};
</script>
<template>
  <input type="number" v-model="number" />
  <button class="button" @click="square">Square of number</button>
  &nbsp;
  <p class="button">{{ number_square }}</p>
  &nbsp;
  <input type="number" v-model="numero_uno" />
  <input type="number" v-model="numero_dos" />
  <button class="button" @click="sum">Sum of numbers</button>
  &nbsp;
  <p class="button" >{{ sum_number }}</p>
  &nbsp;
  <input type="text" v-model="text_uno" />
  <input type="text" v-model="text_dos" />
  <button class="button" @click="swap">Swap values</button>
  &nbsp;
  <input type="text" v-model="fullName" />
  <button class="button" @click="split">Split full name</button>
  <p class="button">Surname  {{ userSurname }}</p>
  <p class="button">Name {{ userName }}</p>
  <p class="button">Patronymic  {{ userPatronymic }}</p>
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
.active {
  border: 7px solid black;
}
.valid {
  color: red;
}

</style>