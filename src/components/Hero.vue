<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";

const roles = ["Android", "iOS", "Web", "Backend", "Design"];
const currentIndex = ref(0);
const currentRole = ref(roles[0]);

let intervalId = null;

const prefersReducedMotion = window.matchMedia(
    "(prefers-reduced-motion: reduce)"
).matches;

onMounted(() => {
    if (prefersReducedMotion) return;

    intervalId = setInterval(() => {
        currentIndex.value = (currentIndex.value +1) % roles.length;
        currentRole.value = roles[currentIndex.value];
    }, 1500); // faster
});

onBeforeUnmount(() => {
    if (intervalId) clearInterval(intervalId);
});
</script>

<template>
    <section id="about" aria-labelledby="about-heading" class="lg: min-h-[500px] flex items-center justify-end px-6 lg:pb-30 pb-4">
        <h1 id="about-heading" class="sr-only">
            About Priscilla
        </h1>

        <img src="../assets/images/avatar.png" alt="Portrait illustration of Priscilla, a mobile and web developer"
                class="rounded-xl avatar" />

        <div class="max-w-5xl w-full bg-gradient-to-t from-[#0b0b14] to-[#14142b]
            rounded-2xl flex flex-col items-end gap-10 p-10 mt-20 lg:mt-58 mx-auto">
            <div class="flex flex-col justify-center space-y-4">
                <p role="text" tabindex="0" class="opacity-80">
                    Hi, I’m Priscilla. You can ask me about
                </p>

                <h2 class="text-4xl lg:text-7xl font-serif relative overflow-hidden h-[1.8em]" aria-live="polite text-center"
                    aria-atomic="true" tabindex="0" aria-label="Android iOS Web Backend Design">
                    <transition name="slide-up" mode="out-in">
                        <span :key="currentRole" class="absolute inset-0 flex items-center" role="text">
                            {{ currentRole }}
                        </span>
                    </transition>
                </h2>

                <!-- Tech list as a list, not decorative spans -->
                <ul class="flex gap-3 mt-6 flex-wrap" role="list" aria-label="Technologies Priscilla works with" tabindex="0">
                    <li>
                        <span
                            class="px-4 py-2 rounded-lg text-sm border border-white/10 bg-[var(--color-card)]">
                            Flutter
                        </span>
                    </li>
                     <li>
                        <span
                            class="px-4 py-2 rounded-lg text-sm border border-white/10 bg-[var(--color-card)]">
                            Vue
                        </span>
                    </li>
                    <li>
                        <span
                            class="px-4 py-2 rounded-lg text-sm border border-white/10 bg-[var(--color-card)]">
                            Node.js
                        </span>
                    </li>
                    <li>
                        <span 
                            class="px-4 py-2 rounded-lg text-sm border border-white/10 bg-[var(--color-card)]">
                            Figma
                        </span>
                    </li>
                    <li>
                        <span
                            class="px-4 py-2 rounded-lg text-sm border border-white/10 bg-[var(--color-card)]">
                            Firebase
                        </span>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style scoped>
.avatar {
    height: 42vw;
    position: absolute;
    top: 3vw;
    left: 15vw;
}

.slide-up-enter-active,
.slide-up-leave-active {
    transition: transform 0.45s ease, opacity 0.35s ease;
}

.slide-up-enter-from {
    transform: translateY(100%);
    opacity: 0;
}

.slide-up-enter-to {
    transform: translateY(0);
    opacity: 1;
}

.slide-up-leave-from {
    transform: translateY(0);
    opacity: 1;
}

.slide-up-leave-to {
    transform: translateY(-100%);
    opacity: 0;
}

@media (prefers-reduced-motion: reduce) {

    .slide-up-enter-active,
    .slide-up-leave-active {
        transition: none;
    }
}

@media screen and (max-width: 480px ){
    #about {
        flex-direction: column;
        flex-wrap: nowrap;
    }
    .avatar{
        height: 60vh;
        position: inherit;
        top: 22vh;
        right: 0;
        margin-top: 42px;
    }
}
</style>
