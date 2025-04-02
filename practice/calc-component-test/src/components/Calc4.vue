<script setup>
import { ref, reactive } from 'vue'
const variant = reactive({ x: 10, y: 20 })
const result = ref(30)
const calcAdd = () => {
  result.value = variant.x + variant.y
}
</script>

<template>
  <div>
    X : <input type="text" v-model.number="variant.x" @change="calcAdd" /> <br />
    Y : <input type="text" v-model.number="variant.y" @change="calcAdd" /> <br />
    <div>결과 : {{ result }}</div>
  </div>
</template>
