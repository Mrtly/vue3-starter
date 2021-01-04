<template>
<div class="text-center mt-10">
  <img class="m-auto" alt="Vue logo" src="./assets/logo.png" /> 
  <CounterExample msg="simple counter in Vue 3 + Vite + TypeScript + Tailwind" />
</div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import CounterExample from "./components/CounterExample.vue";

export default defineComponent({
  name: "App",
  components: {
    CounterExample,
  },
});
</script>
