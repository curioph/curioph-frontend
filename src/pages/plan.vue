<script setup lang="ts">
const user = useUserStore()
const mail = $ref(user.savedName)
const password = $ref(user.savedName)
const router = useRouter()

const login = () => {
  router.push('/plan')
}

const { t } = useI18n()
</script>

<template>
  <div class="mx-auto max-w-80%">
    <div class="flex justify-center">
      <img class="w-25" src="curioph.png" alt="curioph logo" />
    </div>
    <div class="mb-8" />
    <form class="flex flex-col mb-8" @submit.stop.prevent="login">
      <Input v-model="mail" placeholder="xxxxxxx@xxxx.com" />
      <Input v-model="password" type="password" />
      <Button type="submit" class="min-w-40 self-center">{{ t('button.login') }}</Button>
    </form>
    <div class="flex flex-col mb-8">
      <router-link
        class="self-center text-yami font-semibold"
        to="/register"
      >{{ t('link.register') }}</router-link>
      <div class="mb-8" />
      <router-link
        class="self-center text-ajisai"
        to="/forgot-password"
      >{{ t('link.forgot-password') }}</router-link>
    </div>
  </div>
</template>
