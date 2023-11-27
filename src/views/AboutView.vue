<template>
  <div class="about">
    <h1>This is an about page</h1>
    <el-button type="primary" @click="increment">Add:{{ count }}</el-button>
  </div>
</template>

<script setup lang="ts">
import { useCounterStore } from '@/stores/counter'

const counter = useCounterStore()
const { count, increment } = toRefs(counter)
</script>

<style lang="scss">
.about {
  @apply flex flex-col place-items-center text-center;
}
</style>
