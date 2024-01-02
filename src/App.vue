<script setup lang="ts">
import { ref } from 'vue'
import OnceInfo from '@/components/OneInfo.vue'
const propsContent = ref('子コンポーネントにデータを渡すにはPropsを利用する。')
</script>

<template>
  <h1>Props基礎</h1>
  <section>
    <OnceInfo title="Propsの利用" :content="propsContent" />
  </section>
</template>

<style>
section {
  border: blue 1px solid;
  margin: 10px;
}
</style>
