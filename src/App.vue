<script setup lang="ts">
useHead({
  title: 'Curioph',
  meta: [
    { name: 'description', content: 'curiophとは、現実世界の「興味/関心のある行動」と連動し、Web上にコミュニティが出現するサービスです。' },
    {
      name: 'theme-color',
      content: computed(() => isDark.value ? '#00aba9' : '#ffffff'),
    },
  ],
  link: [
    {
      rel: 'icon',
      type: 'image/svg+xml',
      href: computed(() => preferredDark.value ? '/favicon-dark.svg' : '/favicon.svg'),
    },
  ],
})
</script>

<template>
  <RouterView />
</template>
