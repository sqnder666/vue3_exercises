<script>
  export default {
    data() {
	return {
		name: 'чебупели',
    surn: 'вкусные(наверное, не пробовал, просто слово смешное)',
    attr: 'che.jpg',
    text: 'page',
		href: 'page.html',
    num: 5,
    num1: 1,
		num2: 2,
		num3: 6,
    arr1: ['x', 'y', 'z'], 
    arr2: [1, 2, 3], 
	}
}
  }
</script>

<template>
  <div>
		<h1> vue exercises :)</h1>
	</div>
  <br>
  <img :src="attr">
  <div> <p> {{ name }} {{ surn }}</p>
    <p>купи меня пожалуйста <a href="page.html">тут</a></p>
    <p class="sc">Квадрат num равен {{num*num}}, А сумма num1,num2,num3 равна {{num1+num2+num3}}.</p>
    <p class="sc"> Выведем каждую букву из массива в отдельной строке: <br> {{arr1[0]}} <br> {{arr1[1]}} <br> {{arr1[2]}} <br> Теперь сумму элементов второго массива : {{arr2[0] + arr2[1] + arr2[2]}}</p>
  </div>
</template>

<style >
header {
  line-height: 1.5;
}
.sc {
  font-size: medium;
 color: black;
 font-family: 'Lucida Sans Unicode','Lucida Grande','sans-serif';
}
p {
  line-height: 2;
  font-size: medium;
  letter-spacing: 1.2px;
  font-family: 'Lucida Sans Unicode','Lucida Grande','sans-serif';
  color: rgb(0, 0, 0);
}
.logo {
  display: block;
  margin: 0 auto 2rem;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }
  .logo {
    margin: 0 2rem 0 0;
  }
  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>