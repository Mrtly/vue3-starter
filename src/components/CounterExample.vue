<template>
  <div>{{ msg }}</div>
	<button @click='increment' class="mt-4 uppercase px-8 py-2 rounded-full bg-green-300 text-green-600 max-w-max shadow-sm hover:shadow-md">click</button>
  <div class="mt-4 m-auto text-lg text-green-600 max-w-max shadow-sm ">count is: {{ count }}</div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  props: {
    msg: {
      type: String,
      default: 'vite starter'
    }
  },
  setup() {
    let count: number = ref('0');

    function increment(){
      count.value++
    }

    return {
      count, increment
    };
  },
});
</script>
