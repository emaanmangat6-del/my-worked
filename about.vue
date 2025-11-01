<template>
  <div class="min-h-screen bg-gradient-to-b from-black via-zinc-900 to-black text-yellow-300 px-8 py-16 flex flex-col items-center">
    
    <!-- Heading -->
    <h1 class="text-5xl font-extrabold mb-4 text-yellow-400 animate-slide-down">
      About <span class="text-yellow-500">NuxtFit</span>
    </h1>
    <p class="text-lg text-center max-w-2xl text-yellow-200 mb-10 animate-fade-in">
      Welcome to <b>NuxtFit</b> — your daily partner for a balanced, energetic, and healthy lifestyle.  
      We combine fitness, technology, and motivation to help you achieve your best self 💪
    </p>

    <!-- Mission Section -->
    <div class="grid md:grid-cols-2 gap-10 max-w-5xl w-full animate-pop">
      <div class="bg-zinc-950 rounded-2xl p-8 shadow-lg border border-yellow-500/20 hover:border-yellow-500 transition duration-300">
        <h2 class="text-3xl font-bold mb-4 text-yellow-400">🏆 Our Mission</h2>
        <p class="text-yellow-200 leading-relaxed mb-1">
          To empower every individual with the right tools, inspiration, and motivation to lead a fit and confident life.
          We believe that health isn’t a destination — it’s a lifelong journey.
        </p>
      </div>

      <div class="bg-zinc-950 rounded-2xl p-8 shadow-lg border border-yellow-500/20 hover:border-yellow-500 transition duration-300">
        <h2 class="text-3xl font-bold mb-4 text-yellow-400">🌍 Our Vision</h2>
        <p class="text-yellow-200 leading-relaxed mb-1">
          To build a global fitness community where technology meets transformation,  
          and every person feels inspired to move, grow, and glow.
        </p>
      </div>
    </div>

    <!-- Team Image Section -->
    <div class="mt-16 relative animate-float">
      <img
        src="https://images.unsplash.com/photo-1599058917212-d750089bc07e"
        alt="Our Team"
        class="rounded-3xl shadow-2xl w-full max-w-4xl hover:scale-105 transition duration-700"
      />
      <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-transparent rounded-3xl"></div>
    </div>

    <!-- Back Button -->
    <NuxtLink
      to="/"
      class="mt-10 text-yellow-400 hover:text-yellow-300 text-lg transition"
    >
      ← Back to Home
    </NuxtLink>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
@keyframes slide-down {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes fade-in {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes pop {
  0% { transform: scale(0.9); opacity: 0; }
  100% { transform: scale(1); opacity: 1; }
}
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}
.animate-slide-down { animation: slide-down 1s ease-out; }
.animate-fade-in { animation: fade-in 1.2s ease-in-out; }
.animate-pop { animation: pop 0.8s ease-in-out; }
.animate-float { animation: float 3s ease-in-out infinite; }
</style>
