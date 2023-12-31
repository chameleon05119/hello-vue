<script setup lang="ts">
import { ref } from 'vue'

// 時刻の初期化
const now = new Date()
const nowStr = now.toLocaleTimeString()
let timeStr = nowStr
const timeStrRef = ref(nowStr)

// 新しい時刻に変換する関数
function changeTime(): void {
  const newTime = new Date()
  const newTimeStr = newTime.toLocaleTimeString()
  timeStr = newTimeStr
  timeStrRef.value = newTimeStr
}

// 1秒ごとに実行
setInterval(changeTime, 1000)
</script>

<template>
  <p>現在時刻：{{ timeStr }}</p>
  <p>現在時刻(ref)：{{ timeStrRef }}</p>
</template>
