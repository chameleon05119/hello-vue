<script setup lang="ts">
import { ref } from 'vue'
import OnceSection from './components/OnceSection.vue'

const taroProblemslist: string[] = ['電話が通じません。', '留守です。']
const taro = ref('田中太郎')
const taroProblems = ref(taroProblemslist)
const jiro = ref('鈴木二郎')
</script>

<template>
  <section>
    <h2>Slotの利用</h2>
    <OnceSection :name="taro">
      <template #default>
        <p>問題発生</p>
      </template>
      <template #detail>
        <ul>
          <li v-for="problem in taroProblemslist" :key="problem">
            {{ problem }}
          </li>
        </ul>
      </template>
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
