<script setup>
import { useWindowSize } from "@vueuse/core";
import Switcher from "./Switcher.vue";
const { width } = useWindowSize();
</script>

<template>
  <div class="max-w-screen-lg">
    <h2 class="font-medium text-2xl text-center mb-2 max-md:mt-2">
      Выберите рассылки, которые подходят именно вам
    </h2>
    <div class="relative flex justify-center mt-5">
      <input
        class="block w-full rounded-[16px] outline-none m-auto py-4 pl-4 placeholder:text-[#666] max-w-3xl:w-[80%]"
        type="text"
        placeholder="Электронная почта"
      />
      <button
        v-if="width > 768"
        class="absolute z-10 py-4 px-8 bg-[#316fee] text-white rounded-[100px] -right-[1rem] transition-colors hover:bg-[#1a47a1] active:bg-[#316fee]"
      >
        Подписаться
      </button>
      <button
        class="absolute z-10 h-[56px] w-[56px] bg-[#316fee] text-white rounded-[100px] right-[0] translate-x-[12%] transition-colors hover:bg-[#1a47a1]"
        v-else
      >
        <img
          class="m-auto p-3 active:translate-x-4 transition-all"
          src="/arrow.svg"
          alt="arrow"
        />
      </button>
    </div>
    <Switcher size="small">Подписаться на все рассылки</Switcher>
  </div>
</template>
