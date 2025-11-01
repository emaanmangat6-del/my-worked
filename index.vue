
<script setup lang="ts">
</script>

<template>
  <div class="min-h-screen bg-black text-yellow-300 flex flex-col overflow-hidden">
    <!-- Navbar -->
    <nav class="flex justify-between items-center px-8 py-4 bg-zinc-900 shadow-lg border-b border-yellow-500">
      <h1 class="text-3xl font-extrabold text-yellow-400 tracking-wide animate-pulse">NuxtFit</h1>
      <div class="space-x-6 text-lg">
        <NuxtLink to="/" class="hover:text-yellow-500 transition">Home</NuxtLink>
        <NuxtLink to="/tips" class="hover:text-yellow-500 transition">Tips</NuxtLink>
        <NuxtLink to="/about" class="hover:text-yellow-500 transition">About</NuxtLink>
        <NuxtLink to="/contact" class="hover:text-yellow-500 transition">Contact</NuxtLink>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="flex flex-col md:flex-row items-center justify-between grow px-10 py-16 relative">
      <!-- Text -->
      <div class="md:w-1/2 space-y-6 z-10">
        <h2 class="text-5xl md:text-6xl font-extrabold leading-tight animate-fade-in-down">
          Power Up Your <span class="text-yellow-500">Fitness</span> Journey
        </h2>
        <p class="text-lg text-yellow-200 animate-fade-in">
          Your daily source for workout inspiration, diet tips, and lifestyle motivation — built with NUXT fit 💪
        </p>

        <div class="flex gap-4 animate-fade-in-up">
          <UButton color="primary" class="bg-yellow-500 hover:bg-yellow-600 text-black font-bold px-6 py-3 rounded-xl text-lg">
            <NuxtLink to="./tips">Get Started</NuxtLink>
          </UButton>
          <UButton variant="outline" class="border border-yellow-500 text-yellow-400 hover:bg-yellow-500 hover:text-black px-6 py-3 rounded-xl text-lg">
            <NuxtLink to="/about">Know More</NuxtLink>
          </UButton>
        </div>
      </div>

      <!-- Image -->
      <div class="md:w-1/2 mt-10 md:mt-0 relative animate-float">
        <img 
          src="https://images.unsplash.com/photo-1598970434795-0c54fe7c0648"
          alt="Fitness Motivation"
          class="rounded-3xl shadow-2xl hover:scale-105 transition duration-500"
        />
        <div class="absolute inset-0 bg-linear-to-t from-black/70 via-transparent rounded-3xl"></div>
      </div>

      <!-- Background Glow -->
      <div class="absolute w-96 h-96 bg-yellow-500/20 rounded-full blur-3xl top-20 right-10 animate-pulse-slow"></div>
    </section>

    <!-- Footer -->
    <footer class="bg-zinc-950 text-center py-4 text-yellow-500 text-sm tracking-wider">
      © 2025 NuxtFit | All Rights Reserved
    </footer>
  </div>
</template>



<style scoped>
@keyframes fade-in {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes fade-in-down {
  from { opacity: 0; transform: translateY(-30px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes fade-in-up {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-15px); }
}
.animate-fade-in { animation: fade-in 1.2s ease-in-out; }
.animate-fade-in-down { animation: fade-in-down 1.2s ease-out; }
.animate-fade-in-up { animation: fade-in-up 1.2s ease-in-out; }
.animate-float { animation: float 3s ease-in-out infinite; }
.animate-pulse-slow { animation: pulse 3s infinite; }
</style>
