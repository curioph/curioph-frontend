<script lang="ts" setup>
import type { PropType } from 'vue'

const props = defineProps({
  defaultClass: {
    type: String,
    default: '',
  },
  checkedClass: {
    type: String,
    default: '',
  },
  nativeValue: {
    type: String,
    default: '',
  },
  modelValue: {
    type: Array as PropType<string[]>,
    default: () => [],
  },
})
const model = useVModel(props, 'modelValue')

const checked = computed<boolean>(() => model.value.includes(props.nativeValue))
const checkedClass = computed<string>(() => checked.value ? props.checkedClass : props.defaultClass)
</script>

<template>
  <label
    text-xxs cursor-pointer
    peer-checked:border-blue-600 hover:text-gray-600 peer-checked:text-gray-600 hover:bg-gray-50
    :class="checkedClass"
  >
    <slot />
    <input
      v-model="model"
      type="checkbox"
      :value="nativeValue"
      class="hidden peer"
      required=""
      @click.stop
    >
  </label>
</template>

