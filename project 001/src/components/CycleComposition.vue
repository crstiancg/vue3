<template>
    <div>
        <h1>Ciclo de vida, composition API</h1>
    </div>
</template>

<script lang="ts" setup>
import { onMounted, onUpdated, onUnmounted, onBeforeMount } from 'vue';

onBeforeMount(() => {
    console.log("onBeforeMount");
});

onMounted(() => {
    console.log("onMounted");
});
onUpdated(() => {
    console.log("onUpdated");
});

onUnmounted(() => {
    console.log("onUnmounted");
});
</script>

<style scoped>

</style>