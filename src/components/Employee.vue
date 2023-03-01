<script>
import Employee from './components/Employee.vue'
export default {
  data() {
    return {
      developers: [
        {
          id: 1,
          name: 'Ilya',
          salary: 10,
          age: 12
        },
        {
          id: 2,
          name: 'Ilya2',
          salary: 15,
          age: 13
        },
        {
          id: 3,
          name: 'Ilya3',
          salary: 20,
          age: 99
        },
      ],
    }
  },
  components: {
    Employee
  }
}
</script>

<template>
<Employee v-for="developer in developers" :name="developer.name" :salary="developer.salary" :age="developer.age" :key="developer.id" />
</template>

<style>
p,li,ul {
    font-size: 1cm;
    text-align: center;
  text-shadow:
    1px 1px 1px black,
    -1px 1px 1px black;
  color: white;
  transition: all .5s;
}
p,li,ul:hover {
    text-align: center;
    font-size: 1.2cm;
  text-shadow:
    -1px -1px 1px black,
    1px -1px 1px black;
  color: white;
}
</style>