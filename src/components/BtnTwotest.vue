<script setup lang="ts">
import { type Red, ref } from 'vue';

const isActiveClass: Ref<boolean> = ref(true);
</script>

<template>
  <button :class="{ claseB: isActiveClass }">btn</button>
</template>

<style scoped>
.claseB {
  background: green;
}
</style>
