<template>
    <!-- :v-bind:key === :key -->
    <h1 v-for="item in persona" :key="item.id">
        {{ item.id }} {{ item.name }} {{ item.surname }}
    </h1>
</template>

<script setup lang="ts">
// import { ref } from "vue";

// const items = ref([{ message: 'Foo' }, { message: 'Bar' }]);

// const data = ['name', 'age','gender'];

const persona = [
    { 
        id: 1,
        name: 'Paul', 
        surname: 'van Dyk',  
        age: '20', 
        gender: 'Male' 
    }, 
    { 
        id: 2,
        name: 'John', 
        surname: 'Keanu Wick',
        age: '28',
        gender: 'Male',  
    }
    ];
</script>

<style scoped>

</style>