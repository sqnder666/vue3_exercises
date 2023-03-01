<script>
import Employee from "./components/Employee.vue";
export default {
  components: {
    Employee,
  },
};
</script>
<template>
  <Employee :name="['atomic', 'ilya', 'elvin', 'edem', 'edem2', 'gleb']"/>
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