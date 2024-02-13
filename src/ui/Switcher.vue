<script setup>
const props = defineProps({
  size: {
    type: String,
    default: "default",
  },
});
</script>

<template>
  <label class="mt-4 relative inline-flex items-center cursor-pointer">
    <input type="checkbox" value="" class="sr-only peer" />
    <div
      :class="[
        'bg-gray-200',
        'peer-focus:outline-none',
        'peer-focus:shadow-none',
        'peer-focus:ring-4',
        'peer-focus:ring-blue-300',
        'dark:peer-focus:ring-blue-800',
        'rounded-full peer',
        'dark:bg-gray-700',
        'peer-checked:after:translate-x-full',
        'rtl:peer-checked:after:-translate-x-full',
        'peer-checked:after:border-white',
        'after:content-[\'\']',
        'after:start-[2px]',
        'after:bg-white',
        'after:border-gray-300',
        'after:border',
        'after:rounded-full',
        'after:h-5',
        'after:w-5',
        'after:transition-all',
        'dark:border-gray-600',
        'peer-checked:bg-blue-600',
        {
          'w-9': size === 'small',
          'h-5': size === 'small',
          'after:absolute after:top-[0]': size === 'small',
          'after:h-4': size === 'small',
          'after:w-4 ': size === 'small',
          'w-11': size === 'default',
          'h-6': size === 'default',
          'after:absolute after:top-[2px]': size === 'default',
          'after:h-5': size === 'default',
          'after:w-5 ': size === 'default',
          'w-14': size === 'large',
          'h-7': size === 'large',
          'after:top-0.5': size === 'large',
          'after:start-[4px]': size === 'large',
          'after:absolute after:top-[2px]': size === 'large',
          'after:h-6': size === 'large',
          'after:w-6': size === 'large',
        },
      ]"
    ></div>
    <span class="ms-3 text-sm font-medium text-gray-900 dark:text-gray-300"
      ><slot
    /></span>
  </label>
</template>
