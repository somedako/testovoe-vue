<script setup>
import Switcher from "../ui/Switcher.vue";

const props = defineProps({
  data: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <div
    v-for="item in data"
    :key="item.id"
    class="max-w-[476px] m-auto w-full p-6 bg-white rounded-2xl hover:shadow-[0_8px_16px_0_rgba(0,0,0,0.4)] transition-shadow cursor-pointer max-w-lg:p-3"
  >
    <div class="flex justify-between">
      <div>
        <span class="text-xs text-[#999]">{{ item.suptitle }}</span>
        <h2 class="mb-1 text-xl font-semibold">{{ item.title }}</h2>
        <p class="text-sm text-[#666] pr-2">
          {{ item.descr }}
        </p>
      </div>
      <img
        class="rounded-lg max-w-[80px] object-contain"
        :src="item.imgUrl"
        :alt="item.title"
      />
    </div>
    <div class="mt-4">
      <p
        class="text-sm font-medium"
        v-for="(item, ind) in item.checkList"
        :key="ind + 1"
      >
        <span class="inline-block mr-2"
          ><img class="inline-block align-top" src="/check.svg" alt="" /></span
        >{{ item }}
      </p>
    </div>
    <Switcher size="large">Уже получает {{ item.total }} человек</Switcher>
  </div>
</template>
