<template>
  <div class="flex flex-col space-y-3">
    <div v-for="(title, index) in titles" :key="index" class="">
      <div
        class="w-min flex items-center gap-4 hover:cursor-pointer"
        @mouseover="mouseOver(index)"
        @mouseleave="mouseLeave"
      >
        <div
          class="h-2 border-b-2 w-10 transition-all duration-150 ease-linear"
          :class="active && idx == index ? 'w-20 border-slate-200' : 'border-slate-500'"
        ></div>

        <span
          class="text-xs tracking-widest font-bold"
          :class="active && idx == index && 'text-slate-200'"
          >{{ title }}</span
        >
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const active = ref(false);
const titles = ["ABOUT", "EXPERIENCE", "PROJECTS"];
const idx = ref(-1);

const mouseOver = (index) => {
  active.value = true;
  idx.value = index;
};
const mouseLeave = () => {
  active.value = false;
  idx.value = -1;
};
</script>

<style scoped>
.animate {
  transition: all .5s linear;
}
</style>
