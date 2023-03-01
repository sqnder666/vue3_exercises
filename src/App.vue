<script>
import Employee from './components/Employee.vue'
import EmployeeForm from './components/EmployeeForm.vue'
export default {
  data() {
    return {
      developers: [
        {
          id: 1,
          name: 'ilya',
          surn: 'redd'
        },
        {
          id: 2,
          name: 'trippie',
          surn: 'rudov'
        },
        {
          id: 3,
          name: 'playboi',
          surn: 'thugg'
        },
      ],
    }
  },
  components: {
    Developer, EmployeeForm
  },
  methods: {
    add(name, surn){
      let id = this.developers.length + 1;
      this.developers.push({
        id, name, surn
      });
    }
  }
}
</script>

<template>
<EmployeeForm @add="add"/>
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