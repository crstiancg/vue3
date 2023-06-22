<template>
    <div>
        <form action="app" method="get">
            <input type="text" v-model="name">
            <input type="checkbox" v-model="check"> Acepto los terminos
            <select v-model="animals">
                <option value="Tigre">Tigre</option>
                <option value="Leon">Leon</option>
                <option value="Dientes de sable">Dientes de sable</option>
            </select>
        </form>
        <h1>{{ animals }}</h1>
        <h1>{{ name }}</h1>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const name = ref("");
const check = ref(false);

const animals = ref("");

</script>

<style scoped>
input {
    border-color: rgb(8, 207, 161);
    border-radius: 4px;
    height: 1rem;
}
</style>