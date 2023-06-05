<template>
  <a :href="`https://${link}`" class="text-white visited:text-white">
    <slot />
  </a>
</template>

<script setup>
defineProps({
  link: {
    type: String,
    default: 'google.com'
  }
})
</script>

<style lang="scss" scoped>

</style>