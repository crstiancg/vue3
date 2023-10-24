<template>
    <div class="container">
        <PostDetail v-for="data in info" :key="data.title" :title="data.title" :content="data.content"></PostDetail>
    </div>
</template>

<script setup lang="ts">
import PostDetail from './PostDetail.vue';

interface Post {
    id: number,
    title: string,
    content: string
}

const info:Array<Post> = [
    { 
        id: 1,
        title: "primer post", 
        content: "lorem ipsum" 
    },
    { 
        id: 2,
        title: "segundo post", 
        content: "lorem ipsum" 
    },
    { 
        id: 3,
        title: "tercer post", 
        content: "lorem ipsum" 
    },
    { 
        id: 4,
        title: "cuarto post", 
        content: "lorem ipsum" 
    }];
</script>

<style scoped>
.container {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: space-around;
}
</style>