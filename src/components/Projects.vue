<template>
  <section id="projects" aria-labelledby="projects-heading" class="bg-white text-black py-20 px-6 md:px-28">
    <h1 id="projects-heading" class="text-3xl font-serif mb-12" tabindex="0">Recent projects</h1>

    <!-- Project 1 -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center mb-8" tabindex="0">
      <img 
        src="../assets/images/mobile.png" 
        alt="Preview of the Pay Me Blue app" 
        class="rounded-xl shadow-xl w-full md:w-auto"
      />

      <div>
        <h2 class="text-2xl font-semibold">BLUE</h2>
        <p class="mt-4 text-gray-600 leading-relaxed py-8" tabindex="0">
          Experience the future of payments with Blue. Whether you're an individual or a business, our all-in-one platform enables you to send and receive payments effortlessly.
        </p>

        <a href="https://paymeblue.com/app-redirect" target="_blank" rel="noopener noreferrer"
          class="inline-block border border-black px-6 py-3 rounded-lg focus-visible:outline" tabindex="0">
          Get the app
        </a>
      </div>
    </div>

    <!-- Project 2 -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center" tabindex="0">
      <div class="order-2 md:order-1">
        <h2 class="text-2xl font-semibold">Vue Poker App</h2>
        <p class="mt-4 text-gray-600 leading-relaxed py-8" tabindex="0">
          This project uses the Vue framework as well as SCSS and Tailwind to create a beautiful UI 
          and smooth animations
        </p>

        <a href="https://vue-poker-app.netlify.app" target="_blank" rel="noopener noreferrer"
          class="inline-block border border-black px-6 py-3 rounded-lg focus-visible:outline" tabindex="0">
          Try it out
        </a>
      </div>

      <img 
        src="../assets/images/game.png" 
        alt="Preview of the Vue Poker app" 
        class="rounded-xl shadow-xl w-full md:w-auto order-1 md:order-2"
      />
    </div>
  </section>
</template>

