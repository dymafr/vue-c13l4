<template>
  <Suspense>
    <LazyList />
  </Suspense>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from 'vue';

const LazyList = defineAsyncComponent(() => import('./Liste.vue'));
</script>

<style lang="scss"></style>
