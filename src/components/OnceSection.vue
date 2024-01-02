<script setup lang="ts">
interface Props {
  rand: number
}

interface Emits {
  (event: 'createdNewRand'): void
}

defineProps<Props>()
const emit = defineEmits<Emits>()

const onNewRandButtonClink = (): void => {
  emit('createdNewRand')
}
</script>

<template>
  <section class="box">
    <p>子コンポーネントで乱数を表示：{{ rand }}</p>
    <button @click="onNewRandButtonClink">新たな乱数を生成</button>
  </section>
</template>

<style scoped>
.box {
  border: green 1px dashed;
  margin: 10px;
}
</style>
