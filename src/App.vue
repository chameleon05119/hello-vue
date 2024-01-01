<script setup lang="ts">
const mapObj = new Map<number, string>()
mapObj.set(1, 'りんご')
mapObj.set(2, 'みかん')
mapObj.set(3, 'ブドウ')
</script>
<template>
  <ul>
    <li v-for="[id, name] in mapObj" :key="`map-obj-${id}`">
      IDが{{ id }}の果物は{{ name }}です。
    </li>
  </ul>
</template>
