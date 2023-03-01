<script>
export default {
    emits: ['be', 'be2'],
    data() {
        return {
        }
    },
    methods: {
        handle() {
            this.$emit('be');
        },
        handle1() {
            this.$emit('be2');
        },
    }
}
</script>

<template>
<button class="button" @click="handle">pudge</button>
<button class="button" @click="handle1">tp_na_ame</button>
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