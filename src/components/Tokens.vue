<script setup>
import Derivatives from './Derivatives.vue'
import SectionTitle from './SectionTitle.vue'
import TopGainers from './TopGainers.vue'

const title = 'Most Trending Tokens'
const subtitle =
  "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard"

const buttonText = 'Market Overview'
const buttonLink = '/overview'
const buttonBg = '#B4B4B410'
const buttonBorder = '1px solid'
const borderColor = '#B4B4B4'
const buttonTextColor = '#B4B4B4'
const buttonIcon = new URL('@/assets/img/arrowRight.svg', import.meta.url).href
</script>

<template>
  <div class="mb-[120px] mx-auto max-w-screen-xl p-3">
    <SectionTitle
      :title="title"
      :subtitle="subtitle"
      :buttonText="buttonText"
      :buttonLink="buttonLink"
      :buttonBorder="buttonBorder"
      :borderColor="borderColor"
      :buttonBg="buttonBg"
      :buttonTextColor="buttonTextColor"
      :buttonIcon="buttonIcon"
      class="mb-[60px]"
    />

    <div class="lg:flex gap-7">
      <Derivatives class="mb-4 lg:mb-0" />
      <TopGainers />
    </div>
  </div>
</template>
