<script setup>
const props = defineProps({
  breadCrumbs: {
    type: Array,
  },
});
</script>

<template>
  <ul class="flex justify-center gap-6">
    <li
      class="relative text-xs text-[#999] hover:text-[#5b5a5a] transition-colors [&:not(:last-child)]:after:content-['->'] after:absolute after:top-0 after:-right-[1.30rem]"
      v-for="(breadCrumb, ind) in breadCrumbs"
      :key="ind + 1"
    >
      <a :href="breadCrumb.link">{{ breadCrumb.title }}</a>
    </li>
  </ul>
</template>
