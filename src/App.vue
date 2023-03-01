<script>
export default {
  data() {
    return {
      customers: [
        {
          id: 1,
          name: "Ilya",
          value: 10,
          age: 12,
        },
        {
          id: 2,
          name: "Ilya2",
          value: 15,
          age: 13,
        },
        {
          id: 3,
          name: "Ilya3",
          value: 20,
          age: 99,
        },
      ],
    };
  },
  methods: {
    removeItem: function (id) {
      this.customers = this.customers.filter((customer) => {
        return customer.id !== id;
      });
    },
  },
};
</script>
<template>
  <table>
    <tr>
      <th>Id</th>
      <th>Name</th>
      <th>Salary</th>
      <th>Age</th>
      <th>Remove</th>
    </tr>
    <tr v-for="customer in customers">
      <td>{{ customer.id }}</td>
      <td>{{ customer.name }}</td>
      <td>{{ customer.value }}</td>
      <td>{{ customer.age }}</td>
      <td><button class="button" @click="removeItem(customer.id)">remove</button></td>
    </tr>
  </table>
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