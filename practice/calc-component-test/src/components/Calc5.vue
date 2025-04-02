<script setup>
import { watch, ref } from 'vue'
const x = ref(0)
const result = ref(0)

watch(x, (current, old) => {
  console.log(`${old}>${current}`)
  result.value = current + 50000
})
</script>

<template>
  <div>
    x : <input type="text" v-model.number="x" />
    <br />
    결과 : {{ result }}
  </div>
</template>
