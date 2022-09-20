<script setup lang="ts">
import {defineEmits, ref} from "vue";
// defineProps<{msg:string}>();
defineProps({
  msg:String,
  page:Number
})
const count=ref(0)

const emit=defineEmits(['pageFn']);
const butFn=()=>{
  emit('pageFn',5)
}
</script>
<template>
  <h1>{{msg}}</h1>
  <h2>wushibo</h2>
  <h5>
    <button type="button" @click="count++">count is {{count}}</button>
  </h5>
  <button @click="butFn">改变page值：{{page}}</button>
</template>