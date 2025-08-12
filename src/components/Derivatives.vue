<script setup>
import { ref } from 'vue'
import derivatives from '@/constants/derivatives'
import graphRed from '@/assets/img/graphRed.svg'
import graphGreen from '@/assets/img/graphGreen.svg'

const activeTab = ref('derivatives')

const tabs = [
  { id: 'derivatives', label: 'Hot Derivatives', data: derivatives },
  { id: 'coins', label: 'Hot Coins', data: derivatives },
]

const selectTab = (id) => {
  activeTab.value = id
}
</script>

<template>
  <div class="bg-[#1E2329] rounded-lg p-5 max-w-full shadow-md">
    <div class="flex mb-4">
      <button
        v-for="tab in tabs"
        :key="tab.id"
        @click="selectTab(tab.id)"
        :class="[
          'py-2 px-6 font-semibold text-[#FDFDFD] focus:outline-none',
          activeTab === tab.id
            ? 'border-b-2 border-[#FFBE38]'
            : 'text-[#E0E0E0] hover:text-[#FDFDFD]',
        ]"
      >
        {{ tab.label }}
      </button>
    </div>

    <table class="table-fixed text-white w-full">
      <thead>
        <tr class="text-[#E0E0E0] text-[12px] text-center">
          <th class="font-normal text-left pl-2">Trading Pairs</th>
          <th class="font-normal">Last Traded Price</th>
          <th class="font-normal">24H Change</th>
          <th class="font-normal">Charts</th>
          <th class="font-normal">Trade</th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in tabs.find((tab) => tab.id === activeTab).data"
          :key="item.id"
          class="hover-effect text-center"
        >
          <td class="flex items-center py-4 gap-2 pl-2">
            <img :src="item.img" :alt="item.title" class="w-6 h-6 object-contain" />
            <span>{{ item.title }}</span>
          </td>
          <td class="py-4">{{ item.amount }}</td>
          <td class="py-4">
            <span :class="item.negative ? 'text-[#FF4D4F]' : 'text-[#3CCF91]'">
              {{ item.prectnt }}
            </span>
          </td>
          <td class="py-4">
            <img
              :src="item.negative ? graphRed : graphGreen"
              alt="trend icon"
              class="inline-block"
              loading="lazy"
            />
          </td>
          <td class="text-center py-4">
            <button
              class="bg-[#F7A60010] text-[#FFBE38] border border-[#FFBE38] px-3 rounded-md hover_btn"
            >
              Trade
            </button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped>
.hover-effect:hover {
  background: linear-gradient(
    90.04deg,
    rgba(205, 232, 254, 0.05) 0.03%,
    rgba(205, 232, 254, 0) 119.6%
  );
  box-shadow: inset 0px 0px 2.2px rgba(205, 232, 254, 0.25);
  border-radius: 5px;
}

.hover-effect:hover .hover_btn {
  background: #ffbe38;
  color: #1c1c1e;
}
</style>
