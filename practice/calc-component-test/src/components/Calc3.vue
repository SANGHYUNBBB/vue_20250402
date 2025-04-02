<script setup>
import { ref, reactive } from 'vue'
const variant = reactive({ x: 10, y: 20, result: 30 })
const calcAdd = () => {
  variant.result = variant.x + variant.y
}
</script>

<template>
  <div>
    X : <input type="text" v-model.number="variant.x" /><br />
    Y : <input type="text" v-model.number="variant.y" /><br />
    <button @click="calcAdd">계산</button> <br />
    <div>결과 : {{ variant.result }}</div>
  </div>
</template>
