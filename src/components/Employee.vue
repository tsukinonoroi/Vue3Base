<script>
export default {
    props: {
        id: Number,
        name: String,
        surn: String,
    },
    emits: ['change'],
    data() {
        return {
            isEdit: false,
            newName: this.name,
            newSurn: this.surn,
        }
    },
    methods: {
        edit(){
            this.isEdit = true;
        },
        save(){
            this.isEdit = false;
            this.$emit('change', this.id, this.newName, this.newSurn);
        }
    }
}
</script>

<template>
    <template v-if="!isEdit">
    <p class="developer">{{ name }} {{ surn }}</p>
    <button class="button" @click="edit">Изменить</button>
</template>
    <template v-else>
        <input class="text-field__input" v-model="newName">
        <input class="text-field__input" v-model="newSurn">
        <button class="button" @click="save">Сохранить изменения</button>
    </template>
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