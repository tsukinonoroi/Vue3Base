<script>
export default {
    emits: ['morgen', 'morgen1'],
    data() {
        return {
        }
    },
    methods: {
        handleName() {
            this.$emit('morgen', 'Alie Asanova', '18001');
        },
        handleSalary(){
            this.$emit('morgen1', 'Edem Seytumerov', '15999');
        }
    }
}
</script>

<template>
  <button class="button" @click="$emit('morgen', 'Alie Asanova')">Имя</button>
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