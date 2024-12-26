<script setup>
// @name PostDetail
const props = defineProps({
    title: { 
        type: String,
        required: true
    },
    content: { 
        type: String, 
        required: false, 
        default: 'Sin contenido' 
    }
})
const emit = defineEmits(['sayHi'])
const saludar = () =>
{
    emit('sayHi', 'Hoa--');
}
</script>
<style scoped>
    h1{
        color: #00bbaa;
    }
    p{
        color: #00aabb;
    }
    .post{
        margin: 20px;
        padding: 20px;
        border: 1px solid #cccccc;
        background-color: #ffffff;
        border-radius: 10px;
        box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
        transition: background-color 0.3s ease;
    }
</style>
<template>
    <div>
        <h1>{{ title }}</h1>
        <p>{{ content }}</p>
        <button @click="saludar">Di hola</button>
    </div>
</template>