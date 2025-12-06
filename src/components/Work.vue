<template>
  <section class="py-16 text-center">
    <h2 class="text-xl mb-6">I work with…</h2>

    <div class="flex justify-center gap-4 flex-wrap">
      <Chip text="Fintech" />
      <Chip text="Startups" />
      <Chip text="Agencies" />
      <Chip text="Freelance" />
    </div>
  </section>
</template>

<script setup>
import Chip from './WorkChip.vue'
</script>
