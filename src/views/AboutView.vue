<template>
  <div class="about">
    <h1>About</h1>
    <p>{{ count }}</p>
  </div>
</template>

<script setup>
import { storeToRefs } from "pinia";
import { useCounterStore } from "../stores/counter";

const store = useCounterStore();
const { count } = storeToRefs(store);
</script>
