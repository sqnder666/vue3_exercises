<script>
export default {
    props: ['name', 'surname', 'age'],
    data() {
        return {
        }
    }
}
</script>

<template>
<p>{{ name }} 
<br>
{{ surname }} 
<br>
{{ age }}</p>
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