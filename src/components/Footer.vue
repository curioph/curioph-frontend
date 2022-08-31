<script setup lang="ts">
const { t } = useI18n()

const pages = [
  {
    icon: '/img/icn_plan.png',
    label: t('button.plan'),
    to: '/plan',
  },
  {
    icon: '/img/icn_bubble.png',
    label: t('button.bubble'),
    to: '/bubble',
  },
  {
    icon: '/img/icn_connect.png',
    label: t('button.connect'),
    to: '/connect',
  },
  {
    icon: '/img/icn_report.png',
    label: t('button.report'),
    to: '/report',
  },
  {
    icon: '/img/icn_account.png',
    label: t('button.account'),
    to: '/account',
  },
]
</script>

<template>
  <nav text-xxs text-center px-9 py-6 flex justify-between shadow-top rounded-t-10>
    <router-link v-for="page in pages" :to="page.to" :title="page.label">
      <i mb-3 inline-block>
        <img :src="page.icon" :alt="page.label">
      </i>
      <br>
      <span>{{ page.label }}</span>
    </router-link>
  </nav>
</template>

<style scoped>
.router-link-active {
  @apply color-beni;
}
</style>
