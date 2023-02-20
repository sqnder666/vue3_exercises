<script>
export default {
  data() {
    return {};
  },
  methods: {},
};
</script>
<template>
  <p class="button" :style="{ color: 'green', background: 'yellow', fontSize: '30px' }">
    Задание 1
  </p>
  &nbsp; &nbsp; &nbsp;
  <p class="button" :style="{ fontWeight: 'bold', fontStyle: 'italic', fontSize: '30px' }">
    Задание 2
  </p>
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