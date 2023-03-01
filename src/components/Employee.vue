<script>
export default {
    props: {
        name: String, 
        salary: Number, 
        age: Number
    },
    data() {
        return {
        }
    }
}
</script>

<template>
<p>{{ name }} 
<br>
{{ salary }} 
<br>
{{ age }}</p>
</template>



<style>
p {
    font-size: 1cm;
    text-align: center;
  text-shadow:
    1px 1px 1px silver,
    -1px 1px 1px silver;
  color: white;
  transition: all .5s;
}
p:hover {
    text-align: center;
    font-size: 1.2cm;
  text-shadow:
    -1px -1px 1px rgb(252, 1, 1),
    1px -1px 1px rgb(252, 1, 1);
  color: rgb(165, 145, 238);
}
</style>