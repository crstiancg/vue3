<template>
    <div>
        <form action="app.vue" method="get">
            <label>Nombre</label>
            <input type="text" v-model="name">
            <label>Apellido Paterno</label>
            <input type="text" v-model="paterno">
            <label>Apellido Materno</label>
            <input type="text" v-model="materno">

            <label>Genero</label>
            <select v-model="selectgenero">
                <option v-for="item in genero" :key="item.id" :value="item.name">{{item.name}}</option>
            </select>
            <button>Submit</button>
        </form>
        <h1>{{selectgenero}}</h1>
    </div>
</template>

<script setup lang="ts">
import {ref} from "vue";
const name = ref("");
const paterno = ref("");
const materno = ref("");
const genero = ref([
        {
            id: 1,
            name: 'masculino'
        }, 
        { 
            id:2,
            name:'femenino'
        }]);
const selectgenero = ref("");

const save = ref([]);
</script>

<style scoped>

</style>