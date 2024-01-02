<script setup lang="ts">
import { ref, watch, watchEffect } from 'vue'

const obj = ref({
  id: 1,
  name: 'りんご',
  quantity: 0
})
watch(
  () => obj.value.quantity,
  (quantity) => {
    console.log('quantity: ', quantity)
  }
)
watchEffect(() => {
  console.log('watchEffect: ', obj.value.quantity)
})

setInterval(() => {
  obj.value.quantity++
}, 1000)
</script>
