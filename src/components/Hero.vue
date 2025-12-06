<template>
    <section id="about" aria-labelledby="about-heading" class="min-h-screen flex items-center justify-center px-6">
        <h1 id="about-heading" class="sr-only">
            About Priscilla
        </h1>
        <div class="max-w-6xl w-full bg-gradient-to-r from-[#0b0b14] to-[#14142b]
             rounded-2xl grid md:grid-cols-2 gap-10 p-10">

            <img src="../assets/images/avatar.png"
                alt="Portrait illustration of Priscilla, Mobile and Web developer" role="img" />

            <div class="flex flex-col justify-center">
                <p class="opacity-70">Hi, I'm Priscilla. You can ask me about</p>
                <h1 class="text-5xl font-serif mt-3">Android</h1>

                <div class="flex gap-3 mt-6">
                    <span
                        class="px-4 py-2 rounded-lg text-sm border border-white/10 bg-[var(--color-card)]">Flutter</span>
                    <span class="px-4 py-2 rounded-lg text-sm border border-white/10 bg-[var(--color-card)]">Node</span>
                    <span
                        class="px-4 py-2 rounded-lg text-sm border border-white/10 bg-[var(--color-card)]">Figma</span>
                    <span
                        class="px-4 py-2 rounded-lg text-sm border border-white/10 bg-[var(--color-card)]">Firebase</span>
                </div>
            </div>
        </div>
    </section>
</template>
