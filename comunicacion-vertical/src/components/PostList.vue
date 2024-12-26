<script setup>
// @name PostList
import PostDetail from './PostDetail.vue';
let info = [
{
        title: 'post 1', 
        content: 'texto de contenido del post 1'
    },
    {
        title: 'post 2', 
        content: 'texto de contenido del post 2'
    },
    {
        title: 'post 3', 
        content: 'texto de contenido del post 3'
    },
    {
        title: 'post 4', 
        content: 'texto de contenido del post 4'
    },
];
const showAlert = (msg) => { alert(msg) }
</script>
<style scoped>
.container{
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: space-around;
}
</style>

<template>
    <div class="container">
        <PostDetail 
            v-for="inf in info" :key="inf.title" 
            :title="inf.title" 
            :content="inf.content" 
            @sayHi="showAlert"
        />
    </div>
</template>