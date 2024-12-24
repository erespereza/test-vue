<script setup>
    import PostButton from './PostButton.vue'
</script>
<style scoped>
    .post-card{
        border: 1px solid #ccc;
        padding: 10px;
        margin: 10px;
        border-radius: 5px;
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        transition: all 0.3s ease;
    }
</style>
<template>
    <div class="post-card">
        <h3>Titulo</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi, ipsam tenetur sint veniam hic, debitis corporis id sapiente facilis placeat nihil. Sint aspernatur praesentium odio sequi possimus autem tempora doloribus!</p>
        <PostButton />
    </div>
</template>