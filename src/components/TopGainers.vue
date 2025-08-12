<script setup>
import gainers from '@/constants/gainers'
import listings from '@/constants/listings'
import graphRed from '@/assets/img/graphRed.svg'
import graphGreen from '@/assets/img/graphGreen.svg'
</script>

<template>
  <div class="bg-[#1E2329] rounded-lg p-5 lg:max-w-[520px] shadow-md">
    <p class="text-[#FDFDFD] font-medium text-lg mb-4">Top Gainers</p>
    <table class="table-fixed text-white w-full">
      <tbody>
        <tr v-for="gainer in gainers" :key="gainer.id">
          <td class="flex items-center gap-2 py-3">
            <img :src="gainer.img" :alt="gainer.title" class="object-contain" loading="lazy" />
            <span>{{ gainer.title }}</span>
          </td>
          <td class="text-right py-3 font-mono">{{ gainer.amount }}</td>
          <td
            class="text-right py-3 font-semibold"
            :class="gainer.negative ? 'text-[#FF4D4F]' : 'text-[#3CCF91]'"
          >
            {{ gainer.prectnt }}
          </td>
          <td class="text-center py-3">
            <img
              :src="gainer.negative ? graphRed : graphGreen"
              alt="trend icon"
              class="inline-block"
              loading="lazy"
            />
          </td>
        </tr>
      </tbody>
    </table>
    <p class="text-[#FDFDFD] font-medium text-lg mb-4 mt-9">New Listings</p>
    <table class="table-fixed text-white w-full">
      <tbody>
        <tr v-for="list in listings" :key="list.id">
          <td class="flex items-center gap-2 py-3">
            <img :src="list.img" :alt="list.title" class="object-contain" loading="lazy" />
            <span>{{ list.title }}</span>
          </td>
          <td class="text-right py-3 font-mono">{{ list.amount }}</td>
          <td
            class="text-right py-3 font-semibold"
            :class="list.negative ? 'text-[#FF4D4F]' : 'text-[#3CCF91]'"
          >
            {{ list.prectnt }}
          </td>
          <td class="text-center py-3">
            <img
              :src="list.negative ? graphRed : graphGreen"
              alt="trend icon"
              class="inline-block"
              loading="lazy"
            />
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped></style>
