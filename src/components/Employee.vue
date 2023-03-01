<script>
export default {
    props: {
        id: Number,
        name: String,
        surn: String,
    },
    emits: ['remove'],
    data() {
        return {
        }
    },
    methods: {
    }
}
</script>

<template>
    <p>{{ name }} {{ surn }}</p>
    <button class="button" @click="$emit('remove', id)">
        Удали 
    </button>
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