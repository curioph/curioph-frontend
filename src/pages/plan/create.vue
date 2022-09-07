<script setup lang="ts">
const selectedFriends = ref<string[]>([])

interface IAvatar {
  title: string
  image: string
  disabled?: boolean
}

interface IPlan {
  title: string
  sub: string
  image: string
  type: 'midori' | 'beni' | 'yami'
}

const avatars: IAvatar[] = [
  {
    title: 'ワニぞう',
    image: '/user/img_plan01.jpg',
  },
  {
    title: 'curioph1991',
    image: '/user/img_plan01.jpg',
  },
  {
    title: 'WaniMaru',
    image: '/user/img_plan01.jpg',
  },
  {
    title: 'Wani',
    image: '/user/img_plan01.jpg',
  },
]

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
  <header flex justify-end>
    <p py-1 px-3 text-beni text-xxs text-semibold>
      curiophポイント
      <br>
      <span text-2xl>1,000pt</span>
    </p>
  </header>
  <div px-6 py-11 flex flex-col shadow-top rounded-t-10>
    <div flex items-center mb-5>
      <router-link mr-2 to="/plan" title="plan-add">
        <div i-carbon-chevron-left text-2xl />
      </router-link>
      <h1 text-22px>わたしだけのプラン#1</h1>
      <span title="edit-title">
        <div i-carbon-pen text-xl text-gray ml-3 />
      </span>
    </div>
    <div class="friends" flex flex-auto overflow-x-auto gap-x-2 text-ajisai>
      <checkbox-button
        v-for="record in avatars"
        :key="record.title"
        v-model="selectedFriends"
        :native-value="record.title"
        default-class="opacity-40"
        checked-class="opacity-100"
      >
        <avatar
          :title="record.title"
          :image="record.image"
          mb-1
        />
        <p>{{ record.title }}</p>
      </checkbox-button>
      <router-link
        text-xxs
        to="/friends/delete"
      >
        <div i-carbon-add-alt w-10 h-10 mb-1 />
        <p>全て解除</p>
      </router-link>
      <router-link
        text-xxs
        to="/friends/invite"
      >
        <div i-carbon-add-alt w-10 h-10 mb-1 />
        <p>招待する</p>
      </router-link>
    </div>
  </div>
  <plan-bubble />
</template>
