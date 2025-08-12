<script setup>
import bg from '@/assets/img/aboutBg.png'
</script>

<template>
  <div
    class="pt-[60px] pb-[128px] overflow-x-hidden"
    :style="`background-image: url(${bg}); background-size: cover; background-position: center;`"
  >
    <div class="max-w-screen-xl mx-auto p-3">
      <h2 class="text-3xl text-center mb-[60px] font-bold text-[#FDFDFD]">Why Zaptrade?</h2>
      <div class="flex justify-center xl:flex-nowrap flex-wrap items-center">
        <div class="box1">
          <img src="@/assets/img/security.svg" class="mb-5" alt="" />
          <p class="text-[#FDFDFD] font-semibold text-2xl mb-[67px]">Security</p>
          <p class="text-[#E0E0E0] font-normal text-xl">
            Your assets are protected with bank-level encryption and two-factor authentication for
            safe and secure trading.
          </p>
        </div>
        <div class="box2 lg:ml-[-36px]">
          <div class="md:ml-[42px]">
            <img src="@/assets/img/rocket.svg" class="mb-5" alt="" />
            <p class="text-[#FDFDFD] font-semibold text-2xl mb-[67px]">Speed</p>
          </div>
          <p class="text-[#E0E0E0] font-normal text-xl">
            Instant trades, fast deposits & withdrawals.
          </p>
        </div>
        <div class="box3">
          <img src="@/assets/img/support.svg" class="mb-5" alt="" />
          <p class="text-[#FDFDFD] font-semibold text-2xl mb-[67px]">Support</p>
          <p class="text-[#E0E0E0] font-normal text-xl">
            24/7 expert support to help you anytime, anywhere.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.box1 {
  max-width: 591px;
  width: 100%;
  height: 354px;
  background: url(../assets/img/securityBg.png) no-repeat;
  background-size: 100% 100%;
  padding: 41px 91px 50px 35px;
}
.box2 {
  max-width: 363px;
  width: 100%;
  height: 354px;
  background: url(../assets/img/speedBg.png) no-repeat;
  background-size: 100% 100%;
  padding: 40px 23px 35px 35px;
}
.box3 {
  max-width: 365px;
  width: 100%;
  height: 354px;
  background: url(../assets/img/supportBg.png) no-repeat;
  background-size: cover;
  padding: 41px 35px;
}

@media screen and (max-width: 500px) {
  .box1,
  .box2,
  .box3 {
    background: url(../assets/img/supportbg.png) no-repeat;
    background-size: cover;
    padding: 41px 35px;
    width: 100%;
  }

  .box1 {
    max-width: 365px;
    background-size: 100% 100%;
    height: 100%;
  }
}
</style>
