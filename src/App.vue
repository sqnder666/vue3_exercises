<script>
export default {
  data() {
    return {
      obj: {
        done: true,
        selected: false,
      },
    };
  },
  methods: {},
};
</script>
<template>
  <p class="button " :class="obj">tfddfdf</p>
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

.done {
  border: 5px solid black;
}

.selected {
  color: green;
  font-size: 10em;
}
</style>