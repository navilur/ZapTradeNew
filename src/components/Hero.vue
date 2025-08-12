<script setup>
import bg from '@/assets/img/herosection.png'
import coins from '@/constants/hero'
</script>

<template>
  <div
    :style="`background-image: url(${bg}); background-size: cover; background-position: center;`"
    class="w-full xl:h-[849px] h-auto lg:pt-[120px] p-3 overflow-x-hidden relative"
  >
    <video
      src="../assets/img/b-herosections v2.mp4"
      loop
      muted
      autoplay
      class="absolute -z-10 max-w-[1000px] max-h-[1000px] h-fit lg:right-[-200px] mix-blend-screen"
    ></video>
    <div class="max-w-screen-xl mx-auto">
      <div class="xl:flex justify-between">
        <div class="mb-4">
          <h1 class="text-[#FFBE38] text-[36px] md:text-[65px] font-semibold max-w-[658px]">
            Build Wealth with Crypto
          </h1>
          <p class="text-[#E0E0E0] font-normal text-lg max-w-[740px] mb-[73px]">
            Join the growing community on Zaptrade — the trusted destination for effortless crypto
            investing and trading.
          </p>
          <div class="md:flex block gap-4 items-center">
            <div
              class="bg-[#1E2329] min-h-16 p-2 rounded-md gap-2 flex border border-[#4A4A4A] w-full max-w-[492px]"
            >
              <input
                type="text"
                class="w-full h-auto bg-transparent text-white border-none outline-none pl-2"
                placeholder="Email/Phone number"
              />
              <button
                class="bg-[#FFBE38] text-[#1C1C1E] font-semibold px-6 py-2 rounded-md whitespace-nowrap"
              >
                Sign Up
              </button>
            </div>

            <p class="text-[#E0E0E040] text-center my-4">or</p>

            <div
              class="bg-[#1E2329] max-w-[107px] mx-auto md:mx-0 h-16 p-4 rounded-md justify-center items-center gap-4 flex border border-[#4A4A4A]"
            >
              <button>
                <img src="../assets/img/google.svg" alt="" />
              </button>
              <button>
                <img src="../assets/img/apple.svg" alt="" />
              </button>
            </div>
          </div>
        </div>
        <div class="relative xl:block flex flex-wrap gap-3">
          <div
            class="backdrop-blur-md xl:mt-11 py-6 px-5 rounded-lg w-[258px] h-[178px] border border-[#4A4A4A]"
          >
            <div class="flex justify-between items-center">
              <div class="flex gap-3 mb-5">
                <img src="../assets/img/bitcoin2.svg" alt="" />
                <div>
                  <h5 class="font-semibold text-white text-base">Bitcoin</h5>
                  <p class="font-normal text-white/60 text-xs">BTC</p>
                </div>
              </div>
              <img src="../assets/img/arrow-up.svg" alt="" />
            </div>
            <div class="flex justify-between items-center">
              <div>
                <h4 class="text-[21px] text-white font-semibold">$52,291</h4>
                <p class="text-[#3CCF91] font-semibold text-sm">+0.25%</p>
              </div>
              <img src="../assets/img/graph.svg" alt="" />
            </div>
          </div>
          <div
            class="backdrop-blur-md py-6 px-5 xl:mt-[150px] xl:ml-[130px] rounded-lg w-[230.83px] h-[159.25px] border border-[#4A4A4A]"
          >
            <div class="flex justify-between items-center">
              <div class="flex gap-3 mb-5">
                <img src="../assets/img/ethereum2.svg" alt="" />
                <div>
                  <h5 class="font-semibold text-white text-base">Ethereum</h5>
                  <p class="font-normal text-white/60 text-xs">ETH</p>
                </div>
              </div>
              <img src="../assets/img/arrow-up.svg" alt="" />
            </div>
            <div class="flex justify-between items-center">
              <div>
                <h4 class="text-[21px] text-white font-semibold">$28,291</h4>
                <p class="text-[#3CCF91] font-semibold text-sm">+0.25%</p>
              </div>
              <img src="../assets/img/graph.svg" width="99.31" alt="" />
            </div>
          </div>
          <div
            class="backdrop-blur-md py-4 px-3 relative xl:absolute right-[0px] xl:right-[-200px] xl:top-[-50px] rounded-lg w-[164.23px] h-[113.31px] border border-[#4A4A4A]"
          >
            <div class="flex justify-between items-center">
              <div class="flex gap-3 mb-5">
                <img src="../assets/img/litecoin2.svg" width="28.01" height="28.01" alt="" />
                <div>
                  <h5 class="font-semibold text-white text-[10px]">Litecoin</h5>
                  <p class="font-normal text-white/60 text-[7.64px]">ITC</p>
                </div>
              </div>
              <img src="../assets/img/arrow-up.svg" width="11.46" height="11.46" alt="" />
            </div>
            <div class="flex justify-between items-center">
              <div>
                <h4 class="text-base text-white font-semibold">$8,291</h4>
                <p class="text-[#3CCF91] font-semibold text-[8.91px]">+0.25%</p>
              </div>
              <img src="../assets/img/graph.svg" width="70.66" alt="" />
            </div>
          </div>
          <div
            class="backdrop-blur-md p-[10px] relative xl:absolute right-[0px] xl:right-[-250px] xl:top-[150px] rounded-lg w-[123.23px] h-[85.02px] border border-[#4A4A4A]"
          >
            <div class="flex justify-between items-center">
              <div class="flex gap-3 mb-5">
                <img src="../assets/img/litecoin2.svg" width="21.02" height="21.02" alt="" />
                <div>
                  <h5 class="font-semibold text-white text-[7.64px]">Litecoin</h5>
                  <p class="font-normal text-white/60 text-[5.73px]">ITC</p>
                </div>
              </div>
              <img src="../assets/img/arrow-up.svg" width="8.6" height="8.6" alt="" />
            </div>
            <div class="flex justify-between items-center">
              <div>
                <h4 class="text-[10.03px] text-white font-semibold">$8,291</h4>
                <p class="text-[#3CCF91] font-semibold text-[6.69px]">+0.25%</p>
              </div>
              <img src="../assets/img/graph.svg" width="53.02" alt="" />
            </div>
          </div>
          <div
            class="backdrop-blur-md p-[10px] relative xl:absolute right-[0px] xl:right-[-150px] xl:bottom-[150px] rounded-lg w-[109.51px] h-[75.56px] border border-[#4A4A4A]"
          >
            <div class="flex justify-between items-center">
              <div class="flex gap-3 mb-5">
                <img src="../assets/img/litecoin2.svg" width="18.68" height="18.68" alt="" />
                <div>
                  <h5 class="font-semibold text-white text-[6.79px]">Litecoin</h5>
                  <p class="font-normal text-white/60 text-[5.09px]">ITC</p>
                </div>
              </div>
              <img src="../assets/img/arrow-up.svg" width="7.64" height="7.64" alt="" />
            </div>
            <div class="flex justify-between items-center">
              <div>
                <h4 class="text-[8.91px] text-white font-semibold">$8,291</h4>
                <p class="text-[#3CCF91] font-semibold text-[5.94px]">+0.25%</p>
              </div>
              <img src="../assets/img/graph.svg" width="47.12" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
