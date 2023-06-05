<template>
  <div class="w-full hover:bg-hoverBlue px-4 py-3 flex text-sm transition duration-100 ease-in rounded cursor-pointer">
    <div class="w-3/12">{{ `${startDate} - ${endDate}` }}</div>
    <div class="w-1"></div>
    <div class="w-10/12 flex flex-col space-y-3">
      <div class="text-white text-base">{{ jobTitle }}</div>
      <div class="">{{ jobDescription }} Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus sunt, ipsum consequuntur saepe corporis fugit voluptate repellendus molestiae optio sit?></div>
      <div class="flex space-x-1">
        <Cheap v-for="tool in tools" :key="tool">{{ tool }}</Cheap>
      </div>
    </div>
  </div>
</template>

<script setup>
import Cheap from './Cheap.vue'

defineProps({
  startDate: { type: Number, default: 2020 },
  endDate: { type: String, default: 'present' },
  jobTitle: { type: String, default: 'JobTitle' },
  jobDescription: { type: String, default: 'Job description' },
  tools: { type: Object, default: () => ['JS', 'Vue', 'Tailwind'] }
})
</script>

<style lang="scss" scoped>

</style>