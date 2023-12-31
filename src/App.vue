<script setup lang="ts">
import { ref } from 'vue'

const imgAttributes = ref({
  src: '/images/logo.svg',
  alt: 'Vueのロゴ',
  width: 75,
  height: 75
})
</script>

<template>
  <img v-bind="imgAttributes" />
</template>
