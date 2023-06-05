<template>
  <a :href="`https://${link}`" class="text-teal-100 visited:text-teal-100">
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