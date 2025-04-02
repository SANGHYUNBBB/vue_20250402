<template>
  <div>
    <input
      type="checkbox"
      :value="id"
      :checked="checked"
      @change="$emit('check-changed', { id, checked: $event.target.checked })"
    />
    <span v-if="checked === true" style="color: blue; text-decoration: underline">
      <i>{{ label }}</i>
    </span>
    <span v-else style="color: gray">{{ label }}</span>
  </div>
</template>
<script setup>
const props = defineProps(['id', 'checked', 'label'])

const emit = defineEmits(['check-changed'])
// $표시 emit앞에 는 vue 2버전, 옵션방식을 쓸 때까지 사ㅛㅇ하던 방식인데 vue3부터는 안씀.catch((err)=>{
// 그래서 이제는
// const emit으로 사용을 함
// emit 설멍한 거랑 위랑 emit을 맞춰주면 되는거임
</script>
