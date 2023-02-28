<script>
export default {
    props: ['name', 'surn', 'age'],
    data() {
        return {
        }
    }
}
</script>

<template>
   <p class="developer">{{ name }}</p>
   <p class="developer">{{ surn }}</p>
   <p class="developer">{{ age }}</p>
</template>

<style>
p {
    font-size: 1cm;
    text-align: center;
  text-shadow:
    1px 1px 1px silver,
    -1px 1px 1px silver;
  color: white;
  transition: all 0.3333s;
}
p:hover {
    text-align: center;
    font-size: 1.2cm;
  text-shadow:
    -1px -1px 1px silver,
    1px -1px 1px silver;
  color: white;
}
</style>