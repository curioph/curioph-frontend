<script lang="ts" setup>
const props = defineProps({
  title: {
    type: String,
    default: '',
  },
  image: {
    type: String,
    default: '',
  },
  size: {
    type: String,
    default: 'small',
  },
})
</script>

<template>
  <img
    rounded-full w-10 h-10
    :src="props.image"
    :alt="props.title"
  >
</template>

