<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'
import navLinks from '@/constants/nav'

const isMobileMenuOpen = ref(false)
const toggleMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const openSubMenu = ref(null)

const toggleSubMenu = (id) => {
  openSubMenu.value = openSubMenu.value === id ? null : id
}

const showSearch = ref(false)
const toggleSearch = () => {
  showSearch.value = !showSearch.value
}
</script>

<template>
  <nav class="w-full bg-[#0F131D50] text-white xl:px-[80px]">
    <div class="relative flex flex-wrap items-center justify-between mx-auto px-4 py-3">
      <RouterLink to="/" class="flex items-center space-x-3 z-30">
        <img src="@/assets/img/logo.svg" class="h-8" alt="Logo" />
      </RouterLink>

      <div
        :class="[
          'absolute left-1/2 transform -translate-x-1/2 top-full md:static md:top-auto md:transform-none',
          'w-full md:w-auto md:flex items-center justify-center z-10',
          isMobileMenuOpen ? 'block mt-3 bg-[#0F131D] md:bg-transparent' : 'hidden md:block',
        ]"
      >
        <ul
          class="xl:flex flex-col hidden md:flex-row items-center space-y-3 md:space-y-0 md:space-x-8 text-[16px]"
        >
          <li v-for="nav in navLinks" :key="nav.id" class="relative group">
            <RouterLink
              :to="nav.link"
              :class="[
                'block py-2 px-3 hover:text-gray-300',
                nav.subMenu ? 'flex items-center gap-2' : '',
              ]"
            >
              {{ nav.title }}
              <img v-if="nav.subMenu" src="@/assets/img/arrowDown.svg" alt="Dropdown" />
            </RouterLink>

            <ul
              v-if="nav.subMenu"
              class="absolute overflow-hidden left-0 mt-0 w-40 bg-[#0F131D] border border-gray-700 rounded-lg opacity-0 group-hover:opacity-100 group-hover:visible invisible transition duration-200"
            >
              <li
                v-for="(sub, index) in nav.subMenu"
                :key="index"
                class="px-4 py-2 hover:bg-gray-700"
              >
                <RouterLink :to="sub.link" class="block">
                  {{ sub.title }}
                </RouterLink>
              </li>
            </ul>
          </li>
        </ul>
      </div>

      <div class="flex items-center z-30 space-x-4">
        <button class="xl:hidden text-white" @click="toggleMenu">
          <svg
            v-if="!isMobileMenuOpen"
            class="w-6 h-6"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
          </svg>
          <svg
            v-else
            class="w-6 h-6"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>

        <div class="hidden xl:flex items-center space-x-4">
          <div class="relative">
            <button @click="toggleSearch">
              <img src="@/assets/img/searchIcon.svg" class="h-5 w-5" alt="Search" />
            </button>

            <transition name="fade">
              <div
                v-if="showSearch"
                class="absolute top-full right-0 mt-2 text-white bg-[#0F131D] border border-gray-700 rounded-lg p-3 w-64 z-50"
              >
                <input
                  type="text"
                  placeholder="Search..."
                  class="w-full bg-transparent focus:outline-none"
                />
              </div>
            </transition>
          </div>
          <RouterLink
            to="/signup"
            class="py-2 px-9 text-[#1C1C1E] font-semibold rounded-[12px] bg-[#FFBE38]"
          >
            Sign Up
          </RouterLink>
          <RouterLink
            to="/login"
            class="py-2 px-8 text-[#1C1C1E] font-semibold rounded-[12px] bg-[#FDFDFD]"
          >
            Sign In
          </RouterLink>
        </div>
      </div>
    </div>

    <transition name="slide">
      <div
        v-if="isMobileMenuOpen"
        class="fixed max-w-[300px] top-0 pt-14 left-0 h-screen w-[80%] bg-[#0F131D] z-20 p-6 xl:hidden"
      >
        <ul class="space-y-4 text-left">
          <li v-for="nav in navLinks" :key="nav.id" class="relative">
            <div
              v-if="nav.subMenu"
              @click="toggleSubMenu(nav.id)"
              class="flex items-center justify-between cursor-pointer hover:text-gray-300"
            >
              {{ nav.title }}
              <img src="@/assets/img/arrowDown.svg" alt="Dropdown" class="w-4 h-4" />
            </div>

            <RouterLink v-else :to="nav.link" class="block hover:text-gray-300" @click="toggleMenu">
              {{ nav.title }}
            </RouterLink>

            <ul
              v-if="nav.subMenu && openSubMenu === nav.id"
              class="ml-4 mt-2 space-y-2 text-sm border-l border-gray-700 pl-3"
            >
              <li v-for="(sub, index) in nav.subMenu" :key="index" class="hover:text-gray-300">
                <RouterLink :to="sub.link" @click="toggleMenu">{{ sub.title }}</RouterLink>
              </li>
            </ul>
          </li>
        </ul>

        <div class="pt-6 space-y-3">
          <div class="">
            <button @click="toggleSearch">
              <img src="@/assets/img/searchIcon.svg" class="h-5 w-5" alt="Search" />
            </button>

            <transition name="fade">
              <div
                v-if="showSearch"
                class="top-full md:right-0 mt-2 text-white bg-[#0F131D] border border-gray-700 rounded-lg p-3 z-50"
              >
                <input
                  type="text"
                  placeholder="Search..."
                  class="bg-transparent focus:outline-none"
                />
              </div>
            </transition>
          </div>
          <RouterLink
            to="/signup"
            class="block text-center py-2 px-4 text-[#1C1C1E] font-semibold rounded-[12px] bg-[#FFBE38]"
            @click="toggleMenu"
          >
            Sign Up
          </RouterLink>
          <RouterLink
            to="/login"
            class="block text-center py-2 px-4 text-[#1C1C1E] font-semibold rounded-[12px] bg-[#FDFDFD]"
            @click="toggleMenu"
          >
            Sign In
          </RouterLink>
        </div>
      </div>
    </transition>
  </nav>
</template>

<style scoped>
.slide-enter-active,
.slide-leave-active {
  transition: transform 0.3s ease;
}
.slide-enter-from {
  transform: translateX(-100%);
}
.slide-leave-to {
  transform: translateX(-100%);
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
