<script setup lang="ts">
import { ref } from 'vue'
const name = ref('')
</script>

<template>
  <section class="box">
    <input type="text" v-model="name" />
    <p>入力された名前： {{ name }}</p>
  </section>
</template>

<style>
.box {
  border: orange 1px dashed;
  margin: 10px;
}
</style>
