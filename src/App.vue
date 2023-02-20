<script>
export default {
  data() {
    return {
      text: "",
      text_button: "",
      text_array: "",
    };
  },
  methods: {
    split_text: function () {
      this.text_array = this.text_button.split(" ");
    },
  },
};
</script>
<template>
  <textarea v-model="text"></textarea>
  &nbsp;
  <p class="button">{{ text }}</p>
  &nbsp;
  <textarea v-model="text_button"></textarea>
  &nbsp;
  <button class="button" @click="split_text">Array</button>
  &nbsp;
  <ul v-for="elem in text_array">
    <li :key="key">
      {{ elem }}
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
.active {
  border: 7px solid black;
}
.valid {
  color: red;
}

</style>