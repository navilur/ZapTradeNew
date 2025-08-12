<script setup>
import bg from '@/assets/img/footerBg.png'
</script>

<template>
  <div
    class="py-[69px] overflow-x-hidden"
    :style="`background-image: url(${bg}); background-size: cover; background-position: center;`"
  >
    <div class="max-w-screen-xl mx-auto p-3">
      <h2 class="text-3xl mb-[60px] font-bold text-[#FDFDFD]">
        Stay connected. Trade wherever <br />
        you are.
      </h2>
      <div class="lg:flex lg:justify-between items-center">
        <div>
          <div
            class="flex xl:flex-row flex-col mb-[60px] gap-7 text-center lg:text-center justify-between items-center"
          >
            <div class="max-w-[209px] max-h-[209px] p-[22px] border border-[#4A4A4A] rounded-lg">
              <img src="../assets/img/qr.png" alt="" />
            </div>
            <div>
              <p class="text-[#E0E0E0] text-base mb-5">Scan to Download App</p>
              <h4 class="text-[#E0E0E0] font-semibold text-2xl"><u>iOS</u> & <u>Android</u></h4>
            </div>
          </div>
          <div
            class="flex gap-[50px] items-baseline justify-center lg:justify-normal mb-[60px] lg:mb-0"
          >
            <div class="flex flex-col justify-center gap-4">
              <img src="../assets/img/apple2.svg" class="w-[42px] mx-auto" alt="" />
              <p class="text-xl font-normal text-[#E0E0E0]">MacOS</p>
            </div>
            <div class="flex flex-col justify-center gap-4">
              <img src="../assets/img/windows.svg" class="w-[42px] mx-auto" alt="" />
              <p class="text-xl font-normal text-[#E0E0E0]">Windows</p>
            </div>
          </div>
        </div>
        <img
          src="../assets/img/playVideo.png"
          class="max-w-[696.89px] w-full h-full max-h-[392px] mx-auto"
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
