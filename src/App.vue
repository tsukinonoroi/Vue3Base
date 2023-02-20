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
    items: [-1, -2, -3, -4, -5],
    cssClasses: "border: 5px solid red",
    obj: {
        done: true,
        selected: false,
      },
     obj: {
        hidden: true,
      },
    isValid: true,
    isDisabled: true,
    task: "quest",
    task_number: 4,
    number: 1,
      number_square: "Задание 1",
      numero_uno: 0,
      numero_dos: 0,
      sum_number: "Задание 2",
      text_uno: "placeholder",
      text_dos: "placeholder",
      fullName: "",
      userName: "Edem",
      userSurname: "Seytumerov",
      userPatronymic: "Tsuki no noroi",
      text: "abc",
      text_button: "def",
      text_array: "ghi",
      checked: true,
      languages: [],
      choice: "what?",
      english: true,
      russian: false,
      qirimtatar: false,
      selected: "Выберите город",
      dayWeek: "Задание 1",
      dayWeekOptions: [
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday",
        "Saturday",
        "Sunday",
      ],
      dayYear: "",
      dayYearOptions: [
        1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20,
        21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31,
      ],
      monthYear: "",
      monthYearOptions: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12],
      yearYear: "",
      yearYearOptions: [
        2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012,
        2011, 2010, 2009, 2008, 2007, 2006, 2005, 2004, 2003, 2002, 2001, 2000,
      ],
      isDisabled: false,
      var_1: "question one (51)",
      isCtrlPressed: false,
      var_2: "you pressed control + link",
    /* arr: ['Seytumerov', 'Edem', 'Rustemovich'],
    obj: {Seytumerov:'100$', Edem:'200$', Rustemovich:'300$'},
    hrefs: [
        {href: '1.html', text: 'goat'},
        {href: '2.html', text: 'shyne'},
        {href: '3.html', text: 'browdy'},
		  ],
      products: [
      {
				id: 1,
				name: 'product1',
			},
			{
				id: 2,
				name: 'product2',
			},
			{
				id: 3,
				name: 'product3',
			},
		  ]
	} 
}, */
arr: ['a', 'c', 'd'],
    }
  },
  methods: {
    lag: function () {
      this.var_1 = this.$refs.textField.value;
    },
    leg: function (event) {
      if (event.ctrlKey) {
        this.isCtrlPressed = true;
      }
    },
    handleLeftClick: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "left";
      }
    },
    handleRightClick: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "right";
      }
    },
    handleMiddleClick: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "middle";
      }
    },
    split_text: function () {
      this.text_array = this.text_button.split(" "); 
    },
    setDone: function () {
      this.obj.hidden = !this.obj.hidden;
    },
  },  
  methods: {
    add: function() {
		  this.arr.push('b');
  },
    delFirst: function() {
      this.arr.shift();
  },
    delLast: function() {
      this.arr.pop();
  },
    delSecondToLast: function() {
      this.arr.splice(-2, 1);
  },
    sortArr: function() {
      this.arr.sort();
  },
    reverseOrder: function() {
      this.arr.reverse();
  },
  square: function () {
      this.number_square = this.number ** 2;
    },
    sum: function () {
      this.sum_number = this.numero_uno + this.numero_dos;
    },
    swap: function () {
      const temp = this.text_uno;
      this.text_uno = this.text_dos;
      this.text_dos = temp;
    },
    split: function () {
      this.userSurname = this.fullName.split(" ")[0];
      this.userName = this.fullName.split(" ")[1];
      this.userPatronymic = this.fullName.split(" ")[2];
    },
},
computed: {
	price: function() {
		return this.cost *  this.amount;
	}
},
methods: {
  todayDate: function () {
      var today = new Date();
      this.dayYear = String(today.getDate());
      this.monthYear = String(today.getMonth() + 1);
      this.yearYear = today.getFullYear();
    }, 
  eng: function () {
      this.english = true;
      this.russian = false;
      this.qirimtatar = false;
    },
    rus: function () {
      this.english = false;
      this.russian = true;
      this.qirimtatar = false;
    },
    bin: function () {
      this.english = false;
      this.russian = false;
      this.qirimtatar = true;
    },
  setDone: function () {
      this.obj.hidden = !this.obj.hidden;
    },
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
  <p v-for="num in 30">{{ num }}&nbsp;</p>
  </div>
  <div v-for="item in items">		
<p v-if="item >= 0">{{ item }}&nbsp;</p>		
</div>
<ul v-for="smh in products" :key="smh.id">		
	<li>{{ smh.name }}</li>		
	</ul>
  <button class="button" @click.once="add">Задание 1</button>
  <button class="button" @click.once="delFirst">Задание 2</button>
  <button class="button" @click.once="delLast">Задание 3</button>
  <button class="button" @click.once="delSecondToLast">Задание 4</button>
  <button class="button" @click.once="sortArr">Задание 5</button>
  <button class="button" @click.once="reverseOrder">Задание 6</button>
   <button @click="this.obj.hidden = false">hide Задание 2</button>
  <button @click="this.obj.hidden = true">hide Задание 3</button>
  <button @click="setDone">{{ obj.hidden ? "show" : "hide" }} Задание 4</button><br />
  <p>&nbsp;&nbsp;&nbsp;&nbsp;</p>
  <p :class="obj">Задание 1</p>
  <p :class="{active: true, valid: false,}">Phantom</p>
  <p :class="{ active: isValid, valid: isDisabled }">Press2pnick</p>
  <p :style="{ color: 'green', background: 'yellow', fontSize: '30px' }">
    Cometha
  </p>
  &nbsp; &nbsp; &nbsp;
  <p :style="{ fontWeight: 'bold', fontStyle: 'italic', fontSize: '30px' }">
    XXXtentacion
  </p>
  <input type="text" v-model="task" />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <p>{{ task }}</p>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <p>{{ task.toUpperCase() }}</p>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <input type="number" v-model="task_number" />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <p>{{ task_number ** 2 }}</p>

  <div class="red">
    <ul v-for="elem in arr">
      <li>{{ elem }}</li>
    </ul><br>
    <p :style="cssClasses">Hello</p>
    <p :class="obj">Edemchik</p>
  </div>
  <input type="number" v-model="number" />
  <button @click="square">Square of number</button>
  &nbsp;
  <p>{{ number_square }}</p>
  &nbsp;
  <input type="number" v-model="numero_uno" />
  <input type="number" v-model="numero_dos" />
  <button @click="sum">Sum of numbers</button>
  &nbsp;
  <p>{{ sum_number }}</p>
  &nbsp;
  <input type="text" v-model="text_uno" />
  <input type="text" v-model="text_dos" />
  <button @click="swap">Swap values</button>
  &nbsp;
  <input type="text" v-model="fullName" />
  <button @click="split">Split full name</button>
  <p>Surname = {{ userSurname }}</p>
  <p>Name = {{ userName }}</p>
  <p>Patronymic = {{ userPatronymic }}</p>
  <textarea v-model="text"></textarea>
  &nbsp;
  <p>{{ text }}</p>
  &nbsp;
  <textarea v-model="text_button"></textarea>
  &nbsp;
  <button @click="split_text">Array</button>
  &nbsp;
  <ul v-for="elem in text_array">
    <li :key="key">
      {{ elem }}
    </li>
  </ul>
  <input type="checkbox" v-model="checked" />
  &nbsp;
  <p v-if="checked">{{ checked }}</p>
  <input type="checkbox" v-model="languages" value="english" />
  &nbsp;
  <p>English</p>
  &nbsp;
  <input type="checkbox" v-model="languages" value="russian" />
  &nbsp;
  <p>Russian</p>
  <input type="checkbox" v-model="languages" value="javascript" />
  &nbsp;
  <p>JavaScript</p>
  &nbsp;
  <ul v-for="elem in languages">
    <li>{{ elem }}</li>
  </ul>
  <p v-if="english">What is your mother tongue?</p>
  <p v-if="russian">Какой ваш родной язык?</p>
  <p v-if="qirimtatar">Сенинъ ана тили насыл?
    
  </p>
  &nbsp;
  <input
    name="radio"
    type="radio"
    v-model="choice"
    value="English"
    @click="eng"
  />
  &nbsp;
  <input
    name="radio"
    type="radio"
    v-model="choice"
    value="Русский"
    @click="rus"
  />
  &nbsp;
  <input
    name="radio"
    type="radio"
    v-model="choice"
    value="Крымско-татарский"
   @click="rus"
  />
 
  <p>{{ choice }}</p>
  <select v-model="selected">
    <option class="town">Симферополь</option>
    <option class="town">Евпатория</option>
    <option class="town">Феодосия</option>
    <option class="town">Алушта</option>
    <option class="town">Севастополь</option>
    <option class="town">Судак</option>
    <select v-model="dayWeek">
    <option v-for="option in dayWeekOptions">{{ option }}</option>
  </select>
  &nbsp;
  {{ dayWeek }}
  &nbsp;

  <select v-model="dayYear">
    <option v-for="option in dayYearOptions">{{ option }}</option>
  </select>
  <select v-model="monthYear">
    <option v-for="option in monthYearOptions">{{ option }}</option>
  </select>
  <select v-model="yearYear">
    <option v-for="option in yearYearOptions">{{ option }}</option>
  </select>
  &nbsp;
  <button @click="todayDate">Today's date</button>
  </select>

  <p>{{ selected }}</p>
  <input
    type="checkbox"
    :checked="isDisabled"
    @click="($event) => (this.isDisabled = !this.isDisabled)"
  />
  &nbsp;
  <button
    v-bind:disabled="!isDisabled"
    @click="($event) => (this.isDisabled = !this.isDisabled)"
  >
    {{ isDisabled ? "input is enabled" : "input is disabled" }}
  </button>
  <input type="text" @keyup.enter="lag" ref="textField" />
  &nbsp;
  <p>{{ var_1 }}</p>
  &nbsp;
  <a
    href="https://www.youtube.com/watch?v=Dk6TPWUM7TM"
    @click="leg"
    @click.left="handleLeftClick"
    @click.right="handleRightClick"
    @click.middle="handleMiddleClick"
    target="_blank"
    >quesr 2 n 3</a
  >
  &nbsp;
  <p v-if="isCtrlPressed">{{ var_2 }}</p>
</template>

<style>
.town{
  font-style: italic;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  background-color: lightgreen;
}
.active {
  border: 5px solid purple;
}
.valid {
  color: yellow;
}
p.hidden {
  display: none;
}
.done {
  border: 5px solid red;
}
.selected {
  color: green;
  font-size: 10em;
}
red{
  color:red
}
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