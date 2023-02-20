<script>
export default {
  data() {
    return {
      isDisabled: false,
    };
  },
  methods: {},
};
</script>
<template>
  <input
    type="checkbox"
    :checked="isDisabled"
    @click="($event) => (this.isDisabled = !this.isDisabled)"
  />
  &nbsp;
  <button class="button"
    v-bind:disabled="!isDisabled"
    @click="($event) => (this.isDisabled = !this.isDisabled)"
  >
    {{ isDisabled ? "input is enabled" : "input is disabled" }}
  </button>
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