<template>
  <div class="min-h-screen bg-black text-yellow-300 flex flex-col items-center justify-center p-8">
    <h1 class="text-5xl font-extrabold mb-4 animate-slide-down">
      Get in <span class="text-yellow-500">Touch</span>
    </h1>
    <p class="text-center text-lg mb-8 max-w-xl animate-fade-in">
      Have a question, feedback, or collaboration idea?  
      We’d love to hear from you 💬
    </p>

    <!-- Contact Form -->
    <form
      @submit.prevent="handleSubmit"
      class="w-full max-w-md bg-slate-900 rounded-2xl shadow-lg p-6 space-y-4 animate-pop"
    >
      <input
        v-model="name"
        type="text"
        placeholder="Your Name"
        required
        class="w-full p-3 rounded-lg bg-black border border-yellow-500 focus:outline-none focus:ring-2 focus:ring-yellow-400"
      />
      <input
        v-model="email"
        type="email"
        placeholder="Your Email"
        required
        class="w-full p-3 rounded-lg bg-black border border-yellow-500 focus:outline-none focus:ring-2 focus:ring-yellow-400"
      />
      <textarea
        v-model="message"
        placeholder="Your Message"
        rows="4"
        required
        class="w-full p-3 rounded-lg bg-black border border-yellow-500 focus:outline-none focus:ring-2 focus:ring-yellow-400"
      ></textarea>

      <button
        type="submit"
        class="w-full bg-yellow-500 text-black font-semibold py-3 rounded-lg hover:bg-yellow-400 transition duration-300"
      >
        Send Message
      </button>
    </form>

    <!-- Contact Options -->
    <div class="flex flex-col md:flex-row gap-4 mt-10 animate-fade-in">
      <!-- WhatsApp -->
      <a
        :href="`https://wa.me/${whatsappNumber}?text=Hello%20I%20want%20to%20connect%20regarding%20the%20Fitness%20Website!`"
        target="_blank"
        class="flex items-center gap-2 bg-green-500 text-black px-6 py-3 rounded-xl font-bold hover:bg-green-400 transition duration-300"
      >
        💬 WhatsApp Us
      </a>

      <!-- Gmail -->
      <a
        :href="`mailto:${emailAddress}?subject=Fitness%20Website%20Inquiry&body=Hi,%20I%20would%20like%20to%20connect%20about...`"
        class="flex items-center gap-2 bg-red-500 text-white px-6 py-3 rounded-xl font-bold hover:bg-red-400 transition duration-300"
      >
        ✉️ Email Us
      </a>
    </div>

    <!-- Back Button -->
    <NuxtLink
      to="/"
      class="mt-10 inline-block text-yellow-400 hover:text-yellow-300 transition duration-300"
    >
      ← Back to Home
    </NuxtLink>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const message = ref('')

// replace these with your actual contact info
const whatsappNumber = '447000000000' // <- UK format e.g., 447123456789
const emailAddress = 'fitnessweb@gmail.com'

const handleSubmit = () => {
  // You can integrate EmailJS or a backend API here
  alert(`Message sent!\n\nName: ${name.value}\nEmail: ${email.value}\nMessage: ${message.value}`)
  name.value = ''
  email.value = ''
  message.value = ''
}
</script>

<style scoped>
@keyframes slide-down {
  from { opacity: 0; transform: translateY(-20px); }
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
.animate-pop { animation: pop 0.8s ease-in-out; }
</style>
