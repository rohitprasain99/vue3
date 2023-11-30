<script setup lang="ts">
// cannot use primitive values inside reactive
// ref ma .value use garna parxa , reactive ma pardaina
// duitaima return garna paryo
// template ma chai .value use garna pardaina, script vitra matra ho

// better is ref
import { ref } from 'vue'

const count = ref(22)
</script>

<template>
  <main>
    <h2>Counter App</h2>

    <div class="mt-2">count : {{ count }}</div>
    <div class="mt-2">
      <button @click="count++" class="inc-btn">increase</button>
      <button @click="count--" class="dec-btn">decrease</button>
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  height: 100vh;
  width: 100vw;
}

button {
  margin-right: 1rem;
  font-size: 1rem;
  padding: 1rem;
  background: none;
  border: none;
  border-radius: 2rem;

  cursor: pointer;
}

.inc-btn {
  background-color: green;
  color: white;

  &:hover {
    background-color: rgb(98, 210, 98);
    transition: 0.5s ease-out;
  }
}

.dec-btn {
  border: 2px solid red;
  color: red;

  &:hover {
    background-color: rgb(185, 83, 83);
    border: 2px solid rgb(185, 83, 83);
    transition: 0.5s ease-out;
    color: white;
  }
}

.mt-2 {
  margin-top: 1.5rem;
}
</style>
