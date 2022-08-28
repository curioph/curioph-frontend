<script setup lang="ts">
const user = useUserStore()
const mail = $ref(user.savedName)
const password = $ref(user.savedName)

const router = useRouter()
const go = () => {
  router.push(`/hi/${encodeURIComponent(name)}`)
}

const { t } = useI18n()
</script>

<template>
  <div>
    <div text-4xl>
      <img src="curioph.png" alt="curioph logo">
    </div>
    <p>
      Curioph
    </p>
    <p>
      <em text-sm opacity-75>{{ t('intro.desc') }}</em>
    </p>

    <div py-4 />

    <Input v-model="mail" placeholder="xxxxxxx@xxxx.com" />
    <Input v-model="password" type="password" placeholder="" />
    <div>
      <button
        btn m-3 text-sm
        @click="go"
      >
        {{ t('button.go') }}
      </button>
    </div>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
