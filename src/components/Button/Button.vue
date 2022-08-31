<script lang="ts" setup>
import type { PropType } from 'vue'

const props = defineProps({
  label: {
    type: String,
    default: '',
  },
  placeholder: {
    type: String,
    default: '',
  },
  disabled: {
    type: Boolean,
    default: false,
  },
  type: {
    type: String as PropType<'button' | 'submit'>,
    default: 'button',
  },
  modelValue: {
    type: String,
    default: '',
  },
})
</script>

<template>
  <button
    :type="props.type"
    :class="[
      'text-white bg-brand-light hover:bg-brand-dark',
      'font-medium rounded-full text-sm px-5 py-2.5 text-center mr-2 mb-2',
      'focus:outline-none focus:ring-4 focus:bg-brand-dark',
      'dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800',
    ]"
  >
    <slot />
  </button>
</template>

