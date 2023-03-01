<script>
import Employee from './components/Employee.vue'
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
    Employee
  },
  methods: {
    change(id, name, surn){
      this.developers = this.developers.map((developer) => {
        if(developer.id === id){
          developer.name = name;
          developer.surn = surn;
        }
        return developer;
      });
    }
  }
}
</script>

<template>
<Employee v-for   ="developer in developers"
		:id     ="developer.id"
		:name   ="developer.name"
		:surn   ="developer.surn"
		:key    ="developer.id"
    @change="change"/>
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