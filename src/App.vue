<script setup lang="ts">
useHead({
  title: 'Curioph',
  meta: [
    { name: 'description', content: 'curiophとは、現実世界の「興味/関心のある行動」と連動し、Web上にコミュニティが出現するサービスです。' },
    {
      name: 'theme-color',
    },
  ],
  link: [
    {
      rel: 'icon',
      type: 'image/svg+xml',
      href: '/favicon.svg',
    },
  ],
})
</script>

<template>
  <RouterView />
</template>
