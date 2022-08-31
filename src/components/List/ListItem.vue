<script lang="ts" setup>
import type { PropType } from 'vue'

const props = defineProps({
  title: {
    type: String,
    default: '',
  },
  sub: {
    type: String,
    default: '',
  },
  image: {
    type: String,
    default: 'button',
  },
  type: {
    type: String as PropType<'midori' | 'beni' | 'yami'>,
    default: 'beni',
  },
  disabled: {
    type: Boolean,
    default: false,
  },
})

const colorMap = {
  midori: {
    sub: '#5FD0A7',
    title: '#01463E',
    background: '#EAF8F4',
  },
  beni: {
    sub: '#FFA59A',
    title: '#F26262',
    background: '#FFEEEA',
  },
  yami: {
    sub: '#898BD3',
    title: '#2A295B',
    background: '#EFF3F9',
  },
}
</script>

<template>
  <a flex mb-5 :style="{ 'background-color': colorMap[props.type].background }">
    <figure w-28>
      <img w-full h-full object-cover :src="props.image" :alt="props.title" />
    </figure>
    <div flex items-center py-5 px-4>
      <div>
        <h2 text-xl :style="{ 'color': colorMap[props.type].title }">{{ title }}</h2>
        <p :style="{ 'color': colorMap[props.type].sub }">{{ sub }}</p>
      </div>
    </div>
  </a>
</template>

