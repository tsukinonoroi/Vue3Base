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
	}
},
methods: { 
 show: function() { 
  alert(today); 
 }
}
  }
  let today = new Date();   

</script>

<template>
  <div>
		<h1> I'm doing vue project </h1>
	</div>
  <br>
  <img :src="attr">
  <div> <p> Hello, i'm {{ name }} {{ surn }}</p>
    <p>What about <a href="page.html">me?</a></p> <br>
    <p class="sc">Квадрат числа num = {{num*num}}, А сумма чисел num1,num2,num3 = {{num1+num2+num3}}.</p>
    <p class="sc"> Вывод каждой буквы из массива по абзацам: <br> {{arr1[0]}} <br> {{arr1[1]}} <br> {{arr1[2]}} <br>  
      Вывод суммы элементов второго массива : {{arr2[0] + arr2[1] + arr2[2]}}</p>
      <p class="b">Вывод суммы элементов массива obj : {{ obj.x + obj.y + obj.z }} </p>
      <button class="button button1" @click="show">Узнать дату(нажатие)</button> 
    <button class="button button2" @mouseenter="show"> Узнать дату(навестись)</button> 
  </div>
</template>

<style >
header {
  line-height: 1.5;
}
.button1 {
  font-size: medium;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  color:red
}
.button2 {
  font-size: medium;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  color:green
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