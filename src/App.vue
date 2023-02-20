<script>
export default {
  data() {
    return {
      name: "task",
      surname: 1,
    };
  },
  methods: {},
};
</script>
<template>
  <input type="text" v-model="name" />
  <p class="button">{{ name }}</p>
  <p class="button">{{ name.toUpperCase() }}</p>
  <input type="number" v-model="surname" />
  <p class="button">{{ surname ** 2 }}</p>
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