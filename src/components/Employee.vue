<script>
export default {
    data() {
        return {
name: "atomic heart"
        }
    }
}
</script>

<template>
   <p class="developer">{{ name }}</p>
</template>

<style>
p {
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