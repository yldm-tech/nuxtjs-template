<template>
  <div class="flex flex-col justify-center mt-20">
    <h1 class="bg-gray-800 text-white text-center">Click Counter</h1>
    <p class="text-center">You have clicked the button {{ count }} times.</p>
    <button
      @click="counter"
      class="self-center bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
    >
      Click Me!
    </button>
  </div>
</template>

<script setup lang="ts">
import { useCounterStore } from "~/stores";

const { count, increment } = useCounterStore();
const counter = () => {
  console.log("before increment", count);
  increment();
  console.log("after increment", count);
};
</script>
