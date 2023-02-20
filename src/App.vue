<script>
export default {
  data() {
    return {
      var_1: "task1",
      isCtrlPressed: false,
      var_2: "ahhaha",
    };
  },
  methods: {
    lag: function () {
      this.var_1 = this.$refs.textField.value;
    },
    leg: function (event) {
      if (event.ctrlKey) {
        this.isCtrlPressed = true;
      }
    },
    handleLeftClick: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "left";
      }
    },
    handleRightClick: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "right";
      }
    },
    handleMiddleClick: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "middle";
      }
    },
  },
};
</script>
<template>
  <input class="button" type="text" @keyup.enter="lag" ref="textField" />
  &nbsp;
  <p>{{ var_1 }}</p>
  &nbsp;
  <a
  class="button"
    href="https://www.youtube.com/watch?v=xX7kjETpcEM"
    @click="leg"
    @click.left="handleLeftClick"
    @click.right="handleRightClick"
    @click.middle="handleMiddleClick"
    target="_blank"
    >tasks2,3</a
  >
  &nbsp;
  <p v-if="isCtrlPressed">{{ var_2 }}</p>
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