<script setup lang="ts">
const props = defineProps({
  level: {
    type: Number,
    default: 1,
    validator: (v) => {
      return typeof v === 'number' && Number.isInteger(v) && v > 0 && v <= 6
    },
  },
  topClass: {
    type: String,
    default: 'top-10',
    validator: (v) => {
      return typeof v === 'string' && v.match(/^(?:-)?top-(?:\d+|full|(?:\d+\/\d+)|(?:\d+(?:\.\d+)?(?:px|rem)))$/g) !== null
    },
  },
})
</script>

<template>
  <div class="absolute left-0 w-full text-center" :class="topClass">
    <component :is="`h${level}`">
      <slot></slot>
    </component>
  </div>
</template>
