<script setup lang="ts">
const user = useUserStore()
const name = $ref(user.savedName)

const router = useRouter()
const go = () => {
  if (name)
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

    <Input v-model="name" />
    <div>
      <button
        btn m-3 text-sm
        :disabled="!name"
        @click="go"
      >
        {{ t('button.go') }}
      </button>
    </div>
    <p v-for="n in 30">
      Curioph {{ n }}
    </p>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
