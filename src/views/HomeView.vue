<template>
  <div class="home">
    <div class="count">{{ count }}</div>
  </div>
  <div class="buttons">
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <hr />
    <p>This number is doubled: {{ doubleCount }}</p>
    <hr />
    <input type="text" v-model="count" />
  </div>
</template>

<script setup>
import { storeToRefs } from "pinia";
import { useCounterStore } from "../stores/counter";

const store = useCounterStore();
const { count, doubleCount } = storeToRefs(store);

const { increment, decrement } = store;
</script>

<style scoped>
.count {
  font-size: 60px;
  margin: 20px;
}

.buttons button {
  font-size: 40px;
  margin: 10px;
}
</style>
