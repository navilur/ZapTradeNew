<script setup>
import SectionTitle from './SectionTitle.vue'

const title = 'Catch the Next Major Market Move'
const subtitle =
  'Unlock new opportunities with Zaptrade. Stay informed, track market trends, and make your next big trade with confidence and ease.'

const buttonText = 'Explore Now'
const buttonLink = '/features'
const buttonBg = '#FFBE38'
const buttonTextColor = '#1C1C1E'
const buttonIcon = new URL('@/assets/img/arrowUpRight.svg', import.meta.url).href
</script>

<template>
  <div class="mb-[120px] p-3">
    <SectionTitle
      :title="title"
      :subtitle="subtitle"
      :buttonText="buttonText"
      :buttonLink="buttonLink"
      :buttonBg="buttonBg"
      :buttonTextColor="buttonTextColor"
      :buttonIcon="buttonIcon"
    />
  </div>
</template>
