<script setup>

import FiltroNumeros from './components/FiltroNumeros.vue';
const numeros = [0,1,2,3,4,5,6,7,8,9]
</script>
<template>
    <FiltroNumeros :numbersProp="numeros"/>
</template>
