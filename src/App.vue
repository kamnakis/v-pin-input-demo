<script setup lang="ts">
import { ref } from 'vue';

const model = ref('')
const handleCompleted = (val: string) => {
  alert(`Input completed: ${val}`)
}
</script>

<template>
  <pin-input
    v-model="model"
    :length="6"
    class="wrapper"
    input-class="pinInput"
    @completed="handleCompleted"
  />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  display: flex;
  justify-content: center;
  color: #2c3e50;
  margin-top: 60px;
}

.wrapper {
  display: flex;
  gap: 4px;
}

.pinInput {
  width: 20px;
  padding: 4px;
  border: none;
  border-bottom: 3px solid black;
  font-size: 1.5rem;
  color: black;
  margin-right: 4px;
  text-align: center;
  font-weight: 700;
}

.pinInput:focus {
  outline: none;
}
</style>
