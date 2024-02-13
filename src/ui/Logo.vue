<script setup>
const props = defineProps({
  logo: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <a href="/">
    <img :src="logo" class="m-auto pb-10" alt="Logo" />
  </a>
</template>
