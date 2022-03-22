<script setup lang="ts">
import { computed, ref } from 'vue';

const p = defineProps<{ k: string[] }>();

const kandidat = ref('');

const letaKandidat = () => {
  return p.k.filter((k) => {
    return kandidat.indexOf(k) !== -1;
  });
};
</script>

<template>
  <input v-model="kandidat" @input="letaKandidat" />
</template>
