<script lang="ts" setup>
import { useAttrs, onMounted } from 'vue'

const props = defineProps({
  src: {
    type: String,
    default: undefined,
  },
  zoomedX: {
    type: Number,
    default: -240,
  },
  zoomedY: {
    type: Number,
    default: -35,
  },
  scale: {
    type: Number,
    default: 2.1,
  },
  clickIndex: {
    type: Number,
    default: 1,
  },
  maxClickIndex: {
    type: Number,
    default: undefined,
  },
})

const ctx = useAttrs()

function calculateTransform(clicks: number) {
  const isZoomed = (props.maxClickIndex === undefined && clicks === props.clickIndex) || (props.maxClickIndex !== undefined && clicks >= props.clickIndex && clicks <= props.maxClickIndex)
  if (isZoomed)
    return `translate3d(${props.zoomedX}px, ${props.zoomedY}px, 0px) scale(${props.scale})`

  return undefined
}
</script>

<template>
  <img :src="props.src" alt="zoomable image" class="img" :style="{ transform: calculateTransform($slidev.nav.clicks) }" />
</template>

<style scoped>
.img {
  transition: transform 500ms ease;
}
</style>
