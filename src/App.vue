<script setup lang="ts">
import { type Re, ref } from 'vue';

import HelloWorld from './components/HelloWorld.vue';
import BtnTest from './components/BtnTest.vue';
import BtnTwotest from './components/BtnTwotest.vue';

const isActiveClase: Ref<boolean> = ref(true);
</script>

<template>
  <HelloWorld />
  <h2>class externa</h2>
  <BtnTest class="class-2" />
  <h2>:class externa dinamiy</h2>
  <BtnTest class="class-2" :class="{ ['class-3']: isActiveClase }" />
  <h2>:class interna</h2>
  <BtnTwotest class="class-2" :class="{ ['class-3']: isActiveClase }" />
</template>

<style scoped>
.class-2 {
  color: red;
  background: blue;
}

.class-3 {
  border: 2px red solid;
  background: pink;
}
</style>
