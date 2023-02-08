<script>
  export default {
    data() {
	return {
		name: 'Phantom',
		surn: 'Assassin',
    attr: 'pa.jpg',
    text: 'page',
		href: 'page.html',
    num: 5,
    num1: 1,
		num2: 2,
		num3: 3,
    arr1: ['x', 'y', 'z'], 
    arr2: [1, 2, 3], 
    obj: {x: 1, y: 2, z: 3},
    text: 'hellooooooo iwannafly',
    date: '4',
    text1: 'привет',
    cost: 200500,
    amount: 9000,

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
 data: function(){
let date = this.dayOfWeek(this.date);
alert(date);
},
dayOfWeek: function(date){
let days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
return days[date-1];
},
double: function(str){
alert(str*str);
},
change: function(){
		this.text1 = 'привет';
	},
  change2: function(){
    this.text1 = 'делаю аип в 10 вечера'
  },
  change3: function(){
    this.cost = '50'
  },
}
}
  let today = new Date(); 
</script>

<template>
  {{ summ() }}
  <div>
		<h1> I'm doing vue project </h1>
	</div>
  <br>
  <img :src="attr">
  <div> <p> Hello, i'm {{ name }} {{ surn }}</p>
    <p>Значение cost = {{ cost }}, amount = {{ amount  }},Прайс = {{ price }}</p>
    <p>What about <a href="page.html">me?</a></p> <br>
    <p class="sc">Квадрат числа num = {{num*num}}, А сумма чисел num1,num2,num3 = {{num1+num2+num3}}.</p>
    <p class="sc"> Вывод каждой буквы из массива по абзацам: <br> {{arr1[0]}} <br> {{arr1[1]}} <br> {{arr1[2]}} <br>  
      Вывод суммы элементов второго массива : {{arr2[0] + arr2[1] + arr2[2]}}</p>
      <p class="b">Вывод суммы элементов массива obj : {{ obj.x + obj.y + obj.z }} </p>
      <button class="button button1" @click="show">Узнать дату(нажатием)</button> 
    <button class="button button2" @mouseenter="show"> Узнать дату(навестись)</button> <br>
    <button class="button button3" @click="date">Узнать день недели по числу ({{ date }})</button>
    <button class="button" @click="double(2)">Выведет квадрат числа 2</button>
    <button class="button" @click="double(3)">Выведет квадрат числа 3</button>
    <p> {{ text1 }} </p>
    <button @click="change">text</button>
    <button class="button" @click="change">привет</button>
    <button class="button" @click="change2">делаю аип в 10 вечера</button>
    <button @click="change3">Меняем значение cost на 10</button>
  </div>
</template>

<style >
header {
  line-height: 1.5;
}
.button {
    background-color: #000000; 
    border-radius: 8px;
    border: none;
    color: rgb(255, 0, 0);
    padding: 16px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    -webkit-transition-duration: 0.7s; 
    transition-duration: 0.7s;
}

.button1 {
  font-size: medium;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  color:rgb(162, 0, 255)
}
.button2 {
  font-size: medium;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  color:rgb(245, 12, 160)
}
.button3 {
  font-size: medium;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  color:rgb(44, 13, 216)
}
.b {
  font-size:medium;
  color:cornflowerblue;
  font-family: 'Lucida Sans', Geneva, Verdana, sans-serif;
}
.sc {
  font-size: medium;
 color: rgb(48, 113, 255);
 font-style: italic;
}
p {
  line-height: 1.4;
  font-size: large;
  letter-spacing: 2px;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  color: rgb(205, 98, 216);
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