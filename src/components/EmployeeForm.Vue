<script>
export default {
    data() {
        return {
            newName: ' ',
            newSurn: ' ',
        }
    },
    methods: {
        save(){
            this.$emit('add', this.newName, this.newSurn)
        }
    }
}
</script>

<template>
    <input class="button" v-model="newName">
    <br>
    <br>
    <input class="button" v-model="newSurn">
    <br>
    <button class="button" @click="save">save</button>
</template>

<style>
.button {
    background-color: #46ace7; /* Green */
    border-radius: 8px;
    border: none;
    color: rgb(0, 0, 0);
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    -webkit-transition-duration: 0.4s; /* Safari */
    transition-duration: 0.4s;
}
</style>
