<script setup lang="ts">
</script>
<template>
  <button
    class="flex justify-center items-center bg-black border-[1px] border-black min-w-[150px] min-h-[34px] hover:bg-yellow-400 transition-all ease-in duration-100 hover:text-black p-1 rounded-lg text-yellow-400">
    <slot></slot>
  </button>
</template>

<style scoped>
:disabled {
  opacity: 0.15;
  pointer-events: none
}
</style>