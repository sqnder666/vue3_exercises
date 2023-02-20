<script>
export default {
  data() {
    return {
      obj: {
        hidden: true,
      },
    };
  },
  methods: {
    setDone: function () {
      this.obj.hidden = !this.obj.hidden;
    },
  },
}
</script>
<template>
  <button class="button" @click="this.obj.hidden = false">hide 2</button>
  <button class="button" @click="this.obj.hidden = true">hide 3</button>
  <button class="button" @click="setDone">{{ obj.hidden ? "show" : "hide" }} 4</button><br />
  <p>&6hjhjhj;&6hjhjhj;&6hjhjhj;&6hjhjhj;</p>
  <p :class="obj"> 1</p>
</template>
<style>

p.hidden {
  display: none;
} 

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