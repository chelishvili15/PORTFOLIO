<script setup>
import Left from "./components/Left.vue";
import MouseEffect from "./components/MouseEffect.vue";
import Right from "./components/Right.vue";
import { useIsMobile } from "./composable/useIsMobile";

const { isMobile } = useIsMobile();
</script>

<template>
  <div class="flex text-slate-500 px-[10%]" :class="isMobile && 'px-[5%]'">
    <Left class="w-1/2" />
    <Right class="w-1/2" />
    <MouseEffect />
  </div>
</template>

<style scoped></style>
