<template>
  <div class="min-h-screen bg-black text-yellow-300 flex flex-col items-center justify-center p-10 text-center overflow-hidden">
    <h1 class="text-5xl font-extrabold mb-6 animate-slide-down">
      🌐 Project Presentation
    </h1>

    <p class="text-lg max-w-2xl mb-8 animate-fade-in">
      Our fitness web app is designed to inspire and guide users toward a healthier lifestyle.  
      From daily fitness tips to personalized diet plans, the platform blends simplicity with innovation.
    </p>

    <!-- Presentation Section -->
    <div class="bg-zinc-900 border border-yellow-600 rounded-2xl p-8 max-w-4xl w-full shadow-lg mb-10 animate-pop">
      <h2 class="text-3xl font-bold mb-4 text-yellow-400">🎯 Presentation Summary</h2>
      <ul class="text-left space-y-3">
        <li>✨ **Purpose:** Promote a healthy and balanced lifestyle.</li>
        <li>💪 **Features:** Fitness tips, meal plans, workout suggestions, and user interaction.</li>
        <li>🧠 **Technology:** Nuxt 3, Tailwind CSS, and modern animations for sleek UI.</li>
        <li>🚀 **Goal:** To make health & fitness accessible and motivating for everyone.</li>
      </ul>
    </div>

    <!-- Summary Section -->
    <div class="bg-gradient-to-r from-yellow-500 to-yellow-300 text-black rounded-2xl shadow-xl p-8 max-w-3xl animate-fade-up">
      <h2 class="text-3xl font-extrabold mb-4">📋 Project Summary</h2>
      <p class="text-lg leading-relaxed">
        The fitness web app empowers users to take charge of their well-being through  
        curated tips, personalized plans, and a user-friendly design.  
        Built using Nuxt and Tailwind, it’s both functional and visually stunning —  
        encouraging motivation, discipline, and long-term wellness.
      </p>
    </div>

    <!-- Back Buttons -->
    <div class="flex flex-col md:flex-row gap-4 mt-10">
      <NuxtLink
        to="/"
        class="bg-yellow-500 text-black py-3 px-6 rounded-xl font-bold hover:bg-yellow-400 transition duration-300"
      >
        🏠 Back to Home
      </NuxtLink>

      <NuxtLink
        to="/tips"
        class="bg-zinc-900 text-yellow-300 py-3 px-6 rounded-xl font-bold border border-yellow-500 hover:bg-zinc-800 transition duration-300"
      >
        💡 Explore Tips Again
      </NuxtLink>
    </div>
  </div>
</template>

<style scoped>
@keyframes slide-down {
  from { opacity: 0; transform: translateY(-30px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes fade-in {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes fade-up {
  from { opacity: 0; transform: translateY(40px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes pop {
  0% { transform: scale(0.9); opacity: 0; }
  100% { transform: scale(1); opacity: 1; }
}
.animate-slide-down { animation: slide-down 1s ease-out; }
.animate-fade-in { animation: fade-in 1.3s ease-in-out; }
.animate-pop { animation: pop 1s ease-in-out; }
.animate-fade-up { animation: fade-up 1.4s ease-in-out; }
</style>
