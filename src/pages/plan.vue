<script setup lang="ts">
const user = useUserStore()
const mail = $ref(user.savedName)
const password = $ref(user.savedName)
const router = useRouter()

const { t } = useI18n()

const plans = [
  {
    title: 'ワニぞうとのプラン',
    sub: '2022年8月15日作成',
    image: './user/img_plan01.jpg',
    type: 'midori',
  },
  {
    title: 'クロコとのプラン',
    sub: '2022年8月15日作成',
    image: './user/img_plan02.jpg',
    type: 'beni',
  },
  {
    title: 'わたしだけのプラン',
    sub: '2022年8月15日作成',
    image: './user/img_plan03.jpg',
    type: 'yami',
  },
  {
    title: 'ワニぞうとのプラン',
    sub: '2022年8月15日作成',
    image: './user/img_plan01.jpg',
    type: 'midori',
  },
]
</script>

<template>
  <header flex justify-end>
    <p py-1 px-3 text-beni text-xxs text-semibold>curiophポイント
      <br>
      <span text-2xl>1,000pt</span>
    </p>
  </header>
  <div px-6 py-11 flex flex-col shadow-top rounded-t-10 min-h-full> 
    <div flex justify-between items-center mb-5>
      <h1 text-2xl>プランリスト</h1>
      <router-link to="/plan-add" title="plan-add">
        <div i-carbon-add text-4xl />
      </router-link>
    </div>
    <div class="list">
      <list-item
        v-for="plan in plans"
        :type="plan.type"
        :title="plan.title"
        :sub="plan.sub"
        :image="plan.image"
      />
    </div>
  </div>
</template>
