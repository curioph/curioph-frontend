<script setup lang="ts">
interface IPlan {
  title: string
  sub: string
  image: string
  type: 'midori' | 'beni' | 'yami'
}

const plans: IPlan[] = [
  {
    title: 'ワニぞうとのプラン',
    sub: '2022年8月15日作成',
    image: '/user/img_plan01.jpg',
    type: 'midori',
  },
  {
    title: 'クロコとのプラン',
    sub: '2022年8月15日作成',
    image: '/user/img_plan02.jpg',
    type: 'beni',
  },
  {
    title: 'わたしだけのプラン',
    sub: '2022年8月15日作成',
    image: '/user/img_plan03.jpg',
    type: 'yami',
  },
  {
    title: 'ワニぞうとのプラン',
    sub: '2022年8月15日作成',
    image: '/user/img_plan01.jpg',
    type: 'midori',
  },
]
</script>

<template>
  <Header />
  <div px-6 py-11 flex flex-col shadow-top rounded-t-10 min-h-full>
    <div flex justify-between items-center mb-5>
      <h1 text-22px>プランリスト</h1>
      <router-link to="/plan/create" title="plan-add">
        <div i-carbon-add text-4xl />
      </router-link>
    </div>
    <div class="list">
      <list-item
        v-for="plan in plans"
        :key="plan.title"
        :type="plan.type"
        :title="plan.title"
        :sub="plan.sub"
        :image="plan.image"
      />
    </div>
  </div>
</template>
