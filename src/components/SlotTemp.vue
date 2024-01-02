<script setup lang="ts">
import { ref, watch } from 'vue'

const userInput = ref('')
const response = 'あいうえお'
const isMatting = ref(false)
const splitedText = ref({
  splitText1: '',
  splitText2: ''
})

function separateStrings(
  responseText: string,
  userInputText: string
): { splitText1: string; splitText2: string } {
  if (responseText.startsWith(userInputText)) {
    const splitText1 = userInputText
    const splitText2 = responseText.substring(userInputText.length)
    return { splitText1, splitText2 }
  } else {
    // 文字列Bが文字列Aの最初に一致しない場合はA1に空文字列を設定し、A2に全体の文字列Aを設定します。
    return { splitText1: '', splitText2: responseText }
  }
}

watch(
  userInput,
  () => {
    splitedText.value = separateStrings(response, userInput.value)
  },
  { immediate: true }
)
</script>

<template>
  <input type="text" v-model="userInput" />
  <p>isMatting: {{ isMatting }}</p>
  <p>
    <span class="user-input-text">{{ splitedText.splitText1 }}</span>
    <span>{{ splitedText.splitText2 }}</span>
  </p>
</template>

<style scoped>
.user-input-text {
  font-weight: bold;
}
</style>
