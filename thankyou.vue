<template>
  <div class="min-h-screen bg-black text-yellow-400 flex flex-col items-center justify-center p-8 text-center">
    <h1 class="text-6xl font-extrabold mb-6 animate-bounce-slow">
      🎉 Thank You!
    </h1>
    <p class="text-lg mb-8 max-w-xl animate-fade-in">
      Your purchase was successful. Welcome to the <span class="text-yellow-500 font-bold">FitLife Family!</span>  
      We can’t wait for you to start your journey 💪
    </p>

    <div class="flex flex-col md:flex-row gap-4 mt-4">
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
        💡 More Tips
      </NuxtLink>

      <NuxtLink
        to="/webdetails"
        class="bg-gradient-to-r from-yellow-600 to-yellow-400 text-black py-3 px-6 rounded-xl font-extrabold hover:scale-105 transition-transform duration-300"
      >
        🌐 Web Details
      </NuxtLink>
    </div>
  </div>
</template>

<style scoped>
@keyframes fade-in {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes bounce-slow {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-15px); }
}
.animate-fade-in { animation: fade-in 1.2s ease-in-out; }
.animate-bounce-slow { animation: bounce-slow 2s infinite; }
</style>
