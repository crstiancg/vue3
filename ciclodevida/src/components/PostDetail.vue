<template>
    <div class="post">
        <h3>{{ props.title }}</h3>
        <P>{{ props.content }}</P>        
    </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';
const props = defineProps({
    title: String,
    content: String,
});
</script>

<style scoped>
.post {
    width: 300px;
    height: 300px;
    background-color: aquamarine;
    border-radius: 10px;
    margin: 10px;
    padding: 10px;
}
</style>