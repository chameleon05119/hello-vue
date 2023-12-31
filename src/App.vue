<script setup lang="ts">
import { ref } from 'vue'
const bgColor = ref('white')
const onChengeColor = (color: string): void => {
  bgColor.value = color
}
</script>
<template>
  <p v-on:click="onChengeColor('red')" :style="{ backgroundColor: bgColor }">
    クリックすると背景が赤色に変わります
  </p>
</template>
