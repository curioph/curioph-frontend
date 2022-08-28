<script lang="ts" setup>
import { toRefs } from 'vue'
import { useVModel } from '@vueuse/core'
import type { PropType } from 'vue'
import type { InputSize } from '~/components/Input/types'
import { useInputClasses } from '~/components/Input/useInputClasses'

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
    type: String as PropType<'text' | 'password'>,
    default: 'text',
  },
  size: {
    type: String as PropType<InputSize>,
    default: 'md',
  },
  modelValue: {
    type: String,
    default: '',
  },
})
const model = useVModel(props, 'modelValue')
const { labelClasses } = useInputClasses(toRefs(props))
</script>

<template>
  <div class="mb-6">
    <label v-if="label" :class="labelClasses">{{ label }}</label>
    <div class="flex relative">
      <div v-if="$slots.prefix" class="w-10 flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none overflow-hidden">
        <slot name="prefix" />
      </div>
      <input
        v-bind="$attrs"
        v-model="model"
        :disabled="disabled"
        :placeholder="placeholder"
        :type="type"
        :class="[
          'block w-full bg-gray-50 border border-gray-300 text-gray-900 p-2.5 text-sm rounded-16px',
          'focus:ring-blue-500 focus:border-blue-500',
          'dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500',
          $slots.prefix ? 'pl-10' : '',
        ]"
      >
      <div v-if="$slots.suffix" class="absolute right-2.5 bottom-2.5">
        <slot name="suffix" />
      </div>
    </div>
    <p v-if="$slots.helper" class="mt-2 tet-sm text-gray-500 dark:text-gray-400">
      <slot name="helper" />
    </p>
  </div>
</template>

