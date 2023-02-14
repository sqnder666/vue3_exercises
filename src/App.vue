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
		num3: 3,
    arr1: ['x', 'y', 'z'], 
    arr2: [1, 2, 3], 
    obj: {x: 1, y: 2, z: 3},
    date : '2',
    cost: '1760',
    amount: '98',
    visible: true,
    visible1: false,
    hidden: true,
    hidden1: false,
    vue20_1: true,
    vue20_2: true,
    vue20_3: true,
    vue21_1: true,
    cdr: true,
	}
},
computed: {
	price: function() {
		return this.cost *  this.amount;
	}
},
methods: { 
 show: function() { 
  alert(today); 
 },
 summ: function() {
  alert(this.num1 + this.num2)
 },
 hide: function() {
		this.visible = false;
	},
  hide2: function() {
		this.visible = true;
	},
 data: function(){
let date = this.dayOfWeek(this.date);
alert(date);
},
shor: function(){
    alert(new Date().toLocaleDateString());
},
dayOfWeek: function(date){
let days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
return days[date-1];
},
double: function(str){
alert(str*str);
},
change: function(){
		this.text1 = 'батон';
	},
  change2: function(){
    this.text1 = 'свинина'
  },
  change3: function(){
    this.cost = '45'
  },
  toggle: function() {
	this.visible = !this.visible;
  },
  toggle1: function() {
	this.vue20_1 = !this.vue20_1;
  },
  toggle2: function() {
	this.vue20_2 = !this.vue20_2;
  },
  toggle3: function() {
	this.vue20_3 = !this.vue20_3;
  },
  toggle1: function() {
	this.vue21_1 = !this.vue21_1;
  },
}
  }
  let today = new Date(); 
</script>

<template>
   {{ summ() }}
  <div>
		<h1> vue exercises :)</h1>
	</div>
  <br>
  <img :src="attr">
  <div> <p> {{ name }} {{ surn }}</p>
    <p>купи меня пожалуйста <a href="page.html">тут</a></p>
    <p class="sc">Квадрат num равен {{num*num}}, А сумма num1,num2,num3 равна {{num1+num2+num3}}.</p>
    <p class="sc"> Выведем каждую букву из массива в отдельной строке: <br> {{arr1[0]}} <br> {{arr1[1]}} <br> {{arr1[2]}} <br> Теперь сумму элементов второго массива : {{arr2[0] + arr2[1] + arr2[2]}}</p>
    <p class="sc">Выведем сумму элементов obj : {{obj.x + obj.y + obj.z}} </p>
    <button class="button" @click="show">Узнать дату(нажать)</button> <br> 
    <button class="button" @mouseenter="show"> Узнать дату(навестись)</button> 
    <button class="button" @click="date">Узнать день недели по числу({{ date }})</button>
    <button class="button" @click="double(2)">Выведет квадрат числа 2</button>
    <button class="button" @click="double(3)">Выведет квадрат числа 3</button>
    <button class="button" @click="change">батон</button>
    <button class="button" @click="change2">свинина</button>
    <button class="button" @click="change3">Меняем значение cost на 45</button>
    <a class="inline-link-1, button" href="https://www.minecraft.net/ru-ru/download" onclick="event.preventDefault()">Не сработает</a>
    <a class ="button" @click.once="shor">Один раз</a>
    <p class="button" v-if="visible">Видно</p>
    <p class="button" v-if="visible1">Не Видно</p>
    <p class="button" v-if="hidden">баранина</p>
    <p class="button" v-if="!hidden1">человечина</p>
    <p class="button" v-if="visible">что со мной не так</p>
    <button class="button" @click="hide">Убрать абзац</button>
	  <p v-if="visible">text</p>
    <button class="button" @click="hide2">Вернуть абзац</button>
	  <p v-if="visible">text</p>
    <button class="button"  @click="toggle1">toggle1</button>
	  <p v-if="vue20_1">абзац1</p>
    <button class="button" @click="toggle2">toggle2</button>
	  <p v-if="vue20_2">абзац2</p>
    <button class="button" @click="toggle3">toggle3</button>
	  <p v-if="vue20_3">абзац3</p>
    <button class="button" @click="toggle1">
		{{ vue21_1 ? 'hide' : 'show' }}
  </button>
  <p v-if="cdr">ахаха бабаба</p>
    <p v-else>бабаба ахаха</p>

</div>
</template>

<style >

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