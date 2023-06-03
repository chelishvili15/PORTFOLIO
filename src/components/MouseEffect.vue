<template>
  <div
    class="absolute bg-darkBlue rounded-full  -translate-x-1/2 -translate-y-1/2 blur-3xl"
    :style="{
      left: `${x}px` ,
      top: `${y}px`,
      width: '400px',
      height: '400px',  
    }"
  >
    
  </div>
</template>

<script setup>
import { useMouse } from "@vueuse/core";

const {x, y} = useMouse()
</script>

<style lang="scss" scoped></style>
