<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <CounterOption />
  <CounterComposition />
  <PostContainer />
</template>

<script setup>
  import PostContainer from './components/PostContainer.vue';
  import CounterOption from './components/CounterOption.vue';
  import CounterComposition from './components/CounterComposition.vue';
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>