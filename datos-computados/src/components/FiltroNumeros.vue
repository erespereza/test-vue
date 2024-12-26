<script setup>
// @name FiltroNumeros
import { ref, computed, defineProps } from 'vue';

// Definir la prop que recibirá el array de números
const props = defineProps({
  numbersProp: {
    type: Array,
    required: true,
  },
});

// Definir un valor reactivo para el filtro
const filterValue = ref(10); // Filtra números menores que este valor

// Propiedad computada que filtra y devuelve el array con los números menores que `filterValue`
const filteredNumbers = computed(() => {
  return props.numbersProp.filter(num => num < filterValue.value);
});

// Función para actualizar el filtro (por ejemplo, a través de una caja de texto)
const updateFilter = (event) => {
  filterValue.value = parseInt(event.target.value, 10);
};
</script>

<template>
  <div>
    <!-- Caja de texto para ingresar el filtro -->
    <input 
      type="number" 
      v-model="filterValue" 
      placeholder="Filtrar números menores que..." 
    />

    <!-- Mostrar la lista filtrada de números -->
    <ul>
      <li v-for="(number, index) in filteredNumbers" :key="index">
        {{ number }}
      </li>
    </ul>
  </div>
</template>