<template>
  <div class="min-h-screen bg-zinc-950 text-yellow-300 flex flex-col">
    <!-- Navbar -->
    <nav class="flex justify-between items-center px-8 py-4 bg-zinc-900 border-b border-yellow-500">
      <h1 class="text-3xl font-extrabold text-yellow-400 tracking-wide animate-pulse">NuxtFit</h1>
      <NuxtLink to="/" class="hover:text-yellow-500 transition text-lg">← Back</NuxtLink>
    </nav>

    <!-- Header -->
    <header class="text-center mt-12 animate-fade-in-down">
      <h2 class="text-5xl font-extrabold mb-3">Daily Fitness Tips 🏋️‍♀️</h2>
      <p class="text-yellow-200 text-lg">Stay motivated with expert advice and easy home workouts</p>
    </header>

    <!-- Tips Cards -->
    <section class="grid md:grid-cols-3 gap-8 p-10 animate-fade-in-up">
      <div
        v-for="(tip, index) in tips"
        :key="index"
        class="bg-zinc-800 border border-yellow-500 p-6 rounded-3xl hover:scale-105 hover:shadow-lg transition duration-300"
      >
        <img
          :src="tip.image"
          alt="Tip Image"
          class="rounded-2xl mb-4 w-full h-48 object-cover"
        />
        <h3 class="text-2xl font-bold text-yellow-400 mb-2">{{ tip.title }}</h3>
        <p class="text-yellow-200 text-sm mb-4">{{ tip.description }}</p>
        <UButton class="bg-yellow-500 text-black font-semibold px-5 py-2 rounded-xl hover:bg-yellow-600">
          <NuxtLink to="/buy">Buy Plan</NuxtLink>
        </UButton>
      </div>
    </section>

    <!-- Footer -->
    <footer class="text-center py-6 border-t border-yellow-500 text-yellow-400 text-sm mt-auto">
      © 2025 NuxtFit | Transform Yourself Today 💪
    </footer>
  </div>
</template>

<script setup lang="ts">
const tips = [
  {
    title: "Morning Stretch Routine",
    description: "Start your day with light stretches to boost energy and flexibility.",
    image: "https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b"
  },
  {
    title: "Stay Hydrated",
    description: "Drinking enough water improves muscle recovery and metabolism.",
    image: "https://images.unsplash.com/photo-1605296867304-46d5465a13f1"
  },
  {
    title: "15-Minute Fat Burn",
    description: "A short but powerful workout to burn calories and tone your body.",
    image: "https://images.unsplash.com/photo-1594737625785-c0f9f7fc85f9"
  }
];
</script>

<style scoped>
@keyframes fade-in-down {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes fade-in-up {
  from { opacity: 0; transform: translateY(20px); } 
  to { opacity: 1; transform: translateY(0); }
}
.animate-fade-in-down { animation: fade-in-down 1s ease-in-out; }
.animate-fade-in-up { animation: fade-in-up 1.2s ease-in-out; }
</style>
