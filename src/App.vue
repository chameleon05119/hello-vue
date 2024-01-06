<script setup lang="ts">
import { ref } from 'vue'
import OnceSection from './components/OnceSection.vue'

const taro = ref('田中太郎')
const jiro = ref('鈴木二郎')
</script>

<template>
  <section>
    <h2>Slotの利用</h2>
    <OnceSection :name="taro">
      <p>連絡がつきません。</p>
    </OnceSection>
    <OnceSection :name="jiro" />
  </section>
</template>

<style>
section {
  border: blue 1px solid;
  margin: 10px;
}
</style>
