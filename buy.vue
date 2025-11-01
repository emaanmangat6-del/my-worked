<template>
  <div class="min-h-screen bg-black text-yellow-300 flex flex-col items-center justify-center p-8">
    <h1 class="text-5xl font-extrabold mb-4 animate-slide-down">
      Choose Your <span class="text-yellow-500">Fitness Plan</span> 🏋️
    </h1>
    <p class="text-center text-lg mb-10 max-w-xl animate-fade-in">
      Select the perfect plan to power your health and lifestyle goals.  
      Each plan comes with exclusive fitness tips, diet guides & expert advice!
    </p>

    <!-- Pricing Cards -->
    <div class="grid md:grid-cols-3 gap-8 w-full max-w-6xl animate-pop">
      <!-- Basic Plan -->
      <div class="bg-zinc-900 border border-yellow-600 rounded-2xl p-6 hover:scale-105 transition duration-300 shadow-lg">
        <h2 class="text-2xl font-bold mb-2 text-yellow-400">Basic Plan</h2>
        <p class="text-sm mb-4 text-yellow-200">Perfect for beginners</p>
        <ul class="space-y-2 mb-6 text-yellow-300">
          <li>💡 Access to 30 Tips</li>
          <li>🥗 Basic Meal Plan</li>
          <li>🕓 24/7 Support</li>
        </ul>
        <p class="text-3xl font-bold mb-4">$9.99</p>
        <button class="w-full bg-yellow-500 text-black py-2 rounded-lg font-bold hover:bg-yellow-400 transition">
            <NuxtLink to="/thankyou">Buy Now</NuxtLink>
          
        </button>
      </div>

      <!-- Pro Plan -->
      <div class="bg-yellow-500 text-black border border-yellow-600 rounded-2xl p-6 hover:scale-105 transition duration-300 shadow-2xl">
        <h2 class="text-2xl font-extrabold mb-2">Pro Plan</h2>
        <p class="text-sm mb-4 text-zinc-800">For active fitness lovers</p>
        <ul class="space-y-2 mb-6 text-zinc-900">
          <li>🔥 Access to All Tips</li>
          <li>🥗 Full Meal & Workout Plan</li>
          <li>🎥 Video Tutorials</li>
        </ul>
        <p class="text-3xl font-extrabold mb-4">$19.99</p>
        <button class="w-full bg-black text-yellow-400 py-2 rounded-lg font-bold hover:bg-zinc-900 transition">
            <NuxtLink to="/thankyou">Buy Now</NuxtLink>
        
        </button>
      </div>

      <!-- Premium Plan -->
      <div class="bg-zinc-900 border border-yellow-600 rounded-2xl p-6 hover:scale-105 transition duration-300 shadow-lg">
        <h2 class="text-2xl font-bold mb-2 text-yellow-400">Premium Plan</h2>
        <p class="text-sm mb-4 text-yellow-200">For serious athletes</p>
        <ul class="space-y-2 mb-6 text-yellow-300">
          <li>💪 Personalized Coaching</li>
          <li>🍎 Custom Diet & Routine</li>
          <li>📞 1-on-1 Consultation</li>
        </ul>
        <p class="text-3xl font-bold mb-4">$29.99</p>
        <button class="w-full bg-yellow-500 text-black py-2 rounded-lg font-bold hover:bg-yellow-400 transition">
            <NuxtLink to="/thankyou">Buy Now</NuxtLink>
        
        </button>
      </div>
    </div>

    <!-- Back Button -->
    <NuxtLink
      to="/tips"
      class="mt-10 inline-block text-yellow-400 hover:text-yellow-300 transition duration-300"
    >
      ← Back to Tips
    </NuxtLink>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
@keyframes slide-down {
  from { opacity: 0; transform: translateY(-30px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes fade-in {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes pop {
  0% { transform: scale(0.9); opacity: 0; }
  100% { transform: scale(1); opacity: 1; }
}
.animate-slide-down { animation: slide-down 1s ease-out; }
.animate-fade-in { animation: fade-in 1.2s ease-in-out; }
.animate-pop { animation: pop 1s ease-in-out; }
</style>
