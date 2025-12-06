<template>
    <div class="border border-white/10 px-6 py-3 rounded-xl bg-[var(--color-card)]">
        ✔ {{ text }}
    </div>
</template>

<script setup>
defineProps({ text: String })
</script>
