<script setup lang='ts'>
import { useCustomClassProp, useCustomStyleProp } from '../composables'

defineProps({
  dark: Boolean,
  customClass: useCustomClassProp,
  customStyle: useCustomStyleProp,
})
</script>

<template>
  <div class="a-bg a-text-color" :class="[{ dark }, customClass]" :style="customStyle">
    <slot />
  </div>
</template>
