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
    visible: true,
    visible1: false,
    hidden: true,
    hidden1: false,
    vue20_1: true,
    vue20_2: true,
    vue20_3: true,
    vue21_1: true,
    seytumerov: true,
    day: "Вторник", 
    age: 18,
    vue25: true,
    items: [1, 2, 3, 4, 5],
    arr: ['Seytumerov', 'Edem', 'Rustemovich'],
    obj: {Seytumerov:'100$', Edem:'200$', Rustemovich:'300$'},
    hrefs: [
        {href: '1.html', text: 'goat'},
        {href: '2.html', text: 'shyne'},
        {href: '3.html', text: 'browdy'},
		  ],
      products: [
        {
          name: 'product1',
          price: 100,
          quantity: 5
        },
        {
          name: 'product2',
          price: 200,
          quantity: 4
        },
        {
          name: 'product3',
          price: 300,
          quantity: 3
        },
		  ]
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
  hide3: function(){
  this.vue25 = false;
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
    this.cost = '20'
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
    <button @click="change3">Меняем значение cost на 20</button>
    <button @click="toggle1">
		{{ vue21_1 ? 'hide' : 'show' }} </button>
    <a class="inline-link-1" href="https://vk.com/playboiibunny" onclick="event.preventDefault()">Не сработает</a>
    <a @click.once="shor">Сработает один раз</a>
    <p v-if="visible">Показан</p>
    <p v-if="visible1">Не показан</p>
    <p v-if="hidden">Phantomka</p>
    <p v-if="!hidden1">Dota</p>
    <p v-if="visible">ilya rudov my friend no????????</p>
    <button class="button" @click="hide">Убрать абзац</button>
	  <p v-if="visible">text</p>
    <button class="button" @click="hide2">Вернуть абзац</button>
	  <p v-if="visible">text</p>
    <button class="button" @click="toggle1">toggle1</button>
	  <p v-if="vue20_1">google)</p>
    <button class="button" @click="toggle2">toggle2</button>
	  <p v-if="vue20_2">CS</p>
    <button class="button" @click="toggle3">toggle3</button>
	  <p v-if="vue20_3">CEPU</p>
    <p class="gfg" v-if="seytumerov">переменная в которой хранится этот текст - моя фамилия</p>
	<p v-else>---</p>
  <p class="day" v-if="day === 'Понедельник'">Понедельник</p>
    <p class="day" v-if="day === 'Вторник'">Вторник</p>
    <p class="day" v-if="day === 'Среда'">Среда</p>
    <p class="dy" v-if="day === 'Четверг'">Четверг</p>
    <p class="day" v-if="day === 'Пятница'">Пятница</p>
    <p class="day" v-if="day === 'Суббота'">Суббота</p>
    <p class="day" v-if="day === 'Воскресенье'">Воскресенье</p>
    <p v-if="age <= 18">Подросток</p>
    <p v-else-if="19 < age && age < 25">Молодой человек</p>
    <p v-else="age > 26">Мужчина</p>
    <div v-if="vue25">
      <button class="button" @click="hide3">спрячь быстра</button>
    <p>aaaaa</p>
    <p>bbbbs</p>
    <p>gfgfdsfsafsb</p>
    <div class="r" v-for="elem in items">{{ elem }}</div>
    <br>
    <div class="r" v-for="elem in items">{{ elem*elem }}</div>
    <br>
    <ul v-for="elem in items">{{ elem }}</ul>
    <ul v-for="(elem, key) in arr"> {{ key }} {{ elem }}</ul>
  </div>
    
  <ul>
    <li v-for="elem in obj">{{ elem }}</li>
    </ul>
    <br>
    <br>
    <ul>
      <li v-for="(key, elem) in obj"> {{ elem }} - {{ key }}</li>
    </ul>
    <br>
    <br>
    <ul>
      <li v-for="(key, elem, index) in obj"> {{ elem }} - {{ key }} - {{ index }}</li>
    </ul>
    <br>
    <br>
    <ul>
      <li v-for="(key, elem, index) in obj"> {{ elem }} - {{ key }} - {{ index+1 }}</li>
    </ul>
    <div v-for="elem in items">
  <p >{{ elem }}</p>
  </div>
  <br>
  <ul v-for="elem in items">
    <li>{{ elem }}</li>
  </ul>
  <ul v-for="smh in hrefs">
    <li><a href="{{ smh.href }}">{{ smh.text }}</a></li>
  </ul>
  <table v-for="product in products">
    <tr>
      <td>{{ product.name }}</td>
      <td>{{ product.price }}</td>
      <td>{{ product.quantity }}</td>
    </tr>
  </table>
  </div>
</template>

<style >
.r {
  color: yellowgreen;
  background-color: black;
  opacity: 99,99%;
  font-weight: 100;
}
ul {
  color:royalblue
}
header {
  line-height: 1.5;
}
.button {
    background-color: #000000; 
    border-radius: 16px;
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
.gfg{
  font-style: initial;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  color: blue;
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
.day {
  font-size: large;
  opacity: 75%;
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