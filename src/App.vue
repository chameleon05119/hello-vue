<script setup lang="ts">
import { ref } from 'vue'
import OnceSection from '@/components/OnceSection.vue'

const randInt = Math.round(Math.random() * 10)
const rand = ref(randInt)
const onCreateNewRand = (): void => {
  rand.value = Math.round(Math.random() * 10)
}
</script>

<template>
  <section>
    <p>親コンポーネントで乱数を表示：{{ rand }}</p>
    <OnceSection :rand="rand" @created-new-rand="onCreateNewRand" />
  </section>
</template>

<style>
section {
  border: blue 1px solid;
  margin: 10px;
}
</style>
