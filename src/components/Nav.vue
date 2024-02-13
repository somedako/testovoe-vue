<script setup>
import { ref } from "vue";

const activeIndex = ref(0);

const props = defineProps({
  navigations: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <nav class="flex justify-center gap-6">
    <a
      v-for="(navigation, ind) in navigations"
      :key="ind + 1"
      @click="activeIndex = ind"
      :class="[
        'text-[#666]',
        'py-4',
        'transition-colors',
        'hover:text-[#2f80ed]',
        'hover:border-b-[2px]',
        'hover:border-b-[#2f80ed]',
        {
          'text-[#2f80ed]': activeIndex === ind,
          'border-b-[2px]': activeIndex === ind,
          'border-b-[#2f80ed]': activeIndex === ind,
        },
      ]"
      :href="navigation.link"
      >{{ navigation.name }}</a
    >
  </nav>
</template>
