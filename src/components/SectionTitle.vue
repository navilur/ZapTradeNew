<script setup>
defineProps({
  title: String,
  subtitle: String,
  align: {
    type: String,
    default: 'left',
  },
  buttonText: String,
  buttonLink: String,
  buttonBg: {
    type: String,
    default: '#FFBE38',
  },
  buttonTextColor: {
    type: String,
    default: '#1C1C1E',
  },
  buttonIcon: String,
  borderColor: {
    type: String,
    default: 'none',
  },
  buttonBorder: {
    type: String,
    default: 'none',
  },
})
</script>

<template>
  <div :class="`md:flex max-w-screen-xl mx-auto justify-between items-center`">
    <div>
      <h2 class="text-3xl font-bold text-[#FFBE38]">{{ title }}</h2>
      <p class="text-[#FDFDFD] font-normal text-lg mt-2 max-w-[797px]">{{ subtitle }}</p>
    </div>
    <RouterLink
      v-if="buttonText"
      :to="buttonLink"
      class="inline-flex items-center justify-center gap-2 rounded-lg px-6 py-3 mt-4"
      :style="{
        backgroundColor: buttonBg,
        color: buttonTextColor,
        border: buttonBorder,
        borderColor: borderColor,
      }"
    >
      <span>{{ buttonText }}</span>
      <img v-if="buttonIcon" :src="buttonIcon" alt="icon" />
    </RouterLink>
  </div>
</template>
