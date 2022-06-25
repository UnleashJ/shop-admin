<template>
  <div> 首页 </div>
  <p>{{ $store.state.count }}</p>
  <p>{{ store.state.count }}</p>
  <p>{{ $store.state.foo }}</p>
  <img
    src="@/assets/logo.png"
    alt=""
  >
</template>

<script lang="ts" setup>
import { useStore } from '@/store'

const store = useStore()
console.log(store.state.count)
</script>

<style lang="scss" scoped>
</style>
