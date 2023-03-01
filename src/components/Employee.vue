<script>
export default {
    emits: ['show', 'show1'],
    data() {
        return {
        }
    },
    methods: {
        handle() {
            this.$emit('show');
        },
        handle1() {
            this.$emit('show1');
        },
    }
}
</script>

<template>
<button class="button" @click="handle">Python</button>
<button class="button" @click="handle1">CPlusPlus</button>
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