<script>
export default {
    emits: ['be', 'be2'],
    data() {
        return {
        }
    },
    methods: {
        handleName() {
            this.$emit('be', 'atomic heart');
        },
        handleSalary(){
            this.$emit('be2', 'pudge pudges', '95');
        }
    }
}
</script>

<template>
<button class="button" @click="handleName">Имя</button>
<button class="button" @click="handleSalary">Зарплата</button>
</template>

<style>
p{
    font-size: 1cm;
    text-align: center;
  text-shadow:
    1px 1px 1px black,
    -1px 1px 1px black;
  color: white;
  transition: all .5s;
}
p:hover {
    text-align: center;
    font-size: 1.2cm;
  text-shadow:
    -1px -1px 1px black,
    1px -1px 1px black;
  color: white;
}
</style>