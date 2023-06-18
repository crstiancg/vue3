<template>
    <!-- uso de ridectivas v-if - v-else - v-show  -->
    <!-- Uso de v-if es cuando no hay muchos cambios -->
    <!-- Uso de v-show es cuando existe reactividad constante, se agrega un class:display-none en la etiqueta -->
    <!-- <h1 v-if="date > 18">Soy mayor de edad</h1>
    <h1 v-else-if="date = 18">Cumpli los 18 años</h1>
    <h1 v-else>Soy menos de edad</h1> -->
    <h1 v-show="age > 18">Soy mayor de edad</h1>
    <h1 v-show="age < 18">Soy menor de edad</h1>
</template>

<script setup lang="ts">

const age = 50;

</script>

<style scoped>

</style>