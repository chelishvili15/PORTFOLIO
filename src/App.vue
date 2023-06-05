<script setup>
import Left from "./components/Left.vue";
import MouseEffect from "./components/MouseEffect.vue";
import Right from "./components/Right.vue";

</script>

<template>
  <div class="flex text-slate-500 py-32">
    <div class="w-1/2 relative">
      <Left class="fixed translate-x-2/3" />
    </div>
    <div class="w-1/2 min-h-max relative">
      <Right class="w-2/3"/>
    </div>
    <MouseEffect />
  </div>
</template>

<style scoped></style>
