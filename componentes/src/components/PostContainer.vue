<script setup>
    import PostCard from './PostCard.vue'
</script>
<style scoped>
    .post-container{
        border: 1px solid #ccc;
        padding: 20px;
        margin-bottom: 20px;
        border-radius: 5px;
        background-color: white;
        box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
        transition: box-shadow 0.3s ease;
        width: 100%;
        display: flex;
        flex-wrap: wrap;
    }
</style>
<template>
    <div class="post-container">
        <PostCard />
        <PostCard />
        <PostCard />
        <PostCard />
        <PostCard />
        
    </div>
</template>