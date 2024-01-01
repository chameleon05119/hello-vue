<script setup lang="ts">
import { ref } from 'vue'
const isAgreed = ref(false)
</script>
<template>
  <label>
    <input type="checkbox" v-model="isAgreed" />
    同意する
  </label>
  <p>結果: {{ isAgreed }}</p>
</template>
