<script>
import Employee from './components/Employee.vue'
export default {
  data() {
    return {
      
    }
  },
  components: {
    Employee
  },
  methods: {
    pudge() {
      alert('BM, RAPIRA, DAGON');
    },
    tp_na_ame(){
      alert('FLASKA, MANGO, CLARITY')
    }
  }
}
</script>

<template>
<Employee @be="pudge" @be2="tp_na_ame" />
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