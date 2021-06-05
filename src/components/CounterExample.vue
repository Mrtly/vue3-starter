<template>
  <div class="text-xl mb-5">{{ msg }}</div>
  <button
    @click="increment"
    class="mt-4 uppercase font-bold tracking-widest px-8 py-2 rounded-full bg-green-600 text-green-200 max-w-max shadow-sm hover:shadow-md focus:outline-none"
  >
    click
  </button>
  <div class="mt-4 m-auto text-xl font-semibold tracking-wider text-green-600">
    count is: {{ count }}
  </div>
  <button
    @click="reset"
    class="mt-8 px-4 py-1 rounded-full bg-green-200 text-green-600 max-w-max shadow-sm hover:shadow-md focus:outline-none"
  >
    reset
  </button>
</template>

<script setup lang="ts">
import { ref, defineProps } from "vue";

defineProps({
  msg: { type: String, default: "vite starter" },
});

let count: number = ref("0");

function increment() {
  count.value++;
}

function reset() {
  count.value = 0;
}
</script>
