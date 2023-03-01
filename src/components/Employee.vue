<script>
export default {
    props: {
        id: Number,
        name: String,
        surn: String,
    },
    emits: ['remove'],
    data() {
        return {
        }
    },
    methods: {
    }
}
</script>

<template>
    <p>{{ name }} {{ surn }}</p>
    <button class="button" @click="$emit('remove', id)">
        remove
    </button>
</template>

<style>

p{
    font-size: 1cm;
    text-align: center;
  text-shadow:
    1px 1px 1px black,
    -1px 1px 1px black;
  color: white;
  transition: all .6s;
}

p:hover {
    text-align: center;
    font-size: 1.2cm;
  text-shadow:
    -1px -1px 1px black,
    1px -1px 1px black;
  color: white;
}

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