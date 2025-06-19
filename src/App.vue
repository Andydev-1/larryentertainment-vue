<script setup>
import { ref } from 'vue';
const navOpen = ref(false);
</script>

<template>
  <nav
    class="flex flex-col md:flex-row items-center justify-between px-4 md:px-10 py-4 bg-gradient-to-r bg-fuchsia-700 to-pink-600 shadow-md sticky top-0 z-50"
  >
    <div class="flex items-center w-full md:w-auto justify-between">
      <img src="./assets/img/logo1.png" alt="SirLarry Entertainment Logo" class="w-23 h-12 md:w-30 md:h-16 shadow mr-2 md:mr-3" />
      <!-- Hamburger Icon (Mobile) -->
      <button @click="navOpen = !navOpen" class="md:hidden focus:outline-none" aria-label="Toggle navigation">
        <svg v-if="!navOpen" class="w-8 h-8 text-white" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"/></svg>
        <svg v-else class="w-8 h-8 text-white" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/></svg>
      </button>
    </div>
    <!-- Nav Links -->
    <ul :class="['flex-col md:flex-row gap-4 md:gap-8 w-full md:w-auto md:flex', navOpen ? 'flex' : 'hidden', 'md:flex', 'bg-fuchsia-700 md:bg-transparent rounded-lg md:rounded-none mt-4 md:mt-0 p-4 md:p-0 text-center md:text-left']">
      <li><a href="#hero" class="block py-2 md:py-0 text-white hover:text-yellow-300 transition-colors duration-200 font-medium cursor-pointer">Home</a></li>
      <li><a href="#about" class="block py-2 md:py-0 text-white hover:text-yellow-300 transition-colors duration-200 font-medium cursor-pointer">About</a></li>
      <li><a href="#services" class="block py-2 md:py-0 text-white hover:text-yellow-300 transition-colors duration-200 font-medium cursor-pointer">Services</a></li>
      <li><a href="#contact" class="block py-2 md:py-0 text-white hover:text-yellow-300 transition-colors duration-200 font-medium cursor-pointer">Contact</a></li>
    </ul>
  </nav>

  <!-- Hero Section -->
  <section id="hero" class="relative min-h-[60vh] md:min-h-[80vh] flex items-center justify-center text-center bg-cover bg-center px-4" style="background-image: url('https://images.unsplash.com/photo-1464983953574-0892a716854b?auto=format&fit=crop&w=1500&q=80');">
    <div class="bg-black bg-opacity-60 p-6 md:p-10 rounded-xl shadow-lg w-full max-w-2xl mx-auto">
      <h1 class="text-3xl sm:text-4xl md:text-6xl font-extrabold text-white mb-4 md:mb-6 drop-shadow-lg">Unleash the <span class="text-yellow-400">Music</span>.<br/>Experience the <span class="text-pink-400">Entertainment</span>.</h1>
      <p class="text-base sm:text-lg md:text-xl text-gray-200 mb-6 md:mb-8">SirLarry Entertainment brings the party to life with unforgettable music, events, and vibes.</p>
      <a href="#contact" class="inline-block w-32 h-10 md:w-40 bg-yellow-400 hover:bg-yellow-500 text-fuchsia-900 font-bold rounded-full text-base md:text-lg shadow transition flex items-center justify-center">Book Us Now</a>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="py-12 md:py-20 px-4 flex flex-col md:flex-row items-center gap-8 md:gap-10 bg-white">
    <img src="https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?auto=format&fit=crop&w=600&q=80" alt="DJ at work" class="w-full md:w-1/3 rounded-2xl shadow-lg mb-6 md:mb-0" />
    <div class="max-w-xl">
      <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-fuchsia-700 mb-3 md:mb-4">About SirLarry Entertainment</h2>
      <p class="text-base sm:text-lg text-gray-700 mb-3 md:mb-4">We are passionate about music, events, and creating memories. With years of experience in the entertainment industry, our team delivers top-notch DJ, MC, and event planning services for all occasions. Let us make your next event unforgettable!</p>
      <ul class="list-disc list-inside text-gray-600 text-sm sm:text-base">
        <li>Professional DJs & MCs</li>
        <li>State-of-the-art sound & lighting</li>
        <li>Custom event experiences</li>
      </ul>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="py-12 md:py-20 px-4 bg-gradient-to-r from-pink-100 to-fuchsia-100">
    <div class="max-w-5xl mx-auto">
      <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-center text-fuchsia-700 mb-8 md:mb-12">Our Services</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 md:gap-10">
        <div class="bg-white rounded-2xl shadow-lg p-6 md:p-8 flex flex-col items-center">
          <img src="https://media.istockphoto.com/id/2185400789/photo/establishing-footage-with-professional-dj-equipment-on-a-club-stage-mixing-decks-controllers.webp?a=1&b=1&s=612x612&w=0&k=20&c=YyA2J6MztDFMy6xtn_C8in1BAP66FchwbJKcGvlgoNo=" alt="DJ Service" class="w-20 h-20 md:w-28 md:h-28 object-cover rounded-full mb-3 md:mb-4" />
          <h3 class="text-xl md:text-2xl font-semibold text-fuchsia-700 mb-1 md:mb-2">DJ Services</h3>
          <p class="text-gray-600 text-center text-sm md:text-base">From weddings to club nights, our DJs keep the dance floor alive with the best beats and mixes.</p>
        </div>
        <div class="bg-white rounded-2xl shadow-lg p-6 md:p-8 flex flex-col items-center">
          <img src="https://media.istockphoto.com/id/2210531481/photo/onstage-portrait-of-black-chanteuse-fronting-jazz-band.webp?a=1&b=1&s=612x612&w=0&k=20&c=rxOin3uWSQEfN6Hpv0h3fp7ZsaMf_llBrZ2PYr7-vt0=" alt="Live Band" class="w-20 h-20 md:w-28 md:h-28 object-cover rounded-full mb-3 md:mb-4" />
          <h3 class="text-xl md:text-2xl font-semibold text-fuchsia-700 mb-1 md:mb-2">Live Bands</h3>
          <p class="text-gray-600 text-center text-sm md:text-base">Book talented live bands for a vibrant, energetic atmosphere at your event.</p>
        </div>
        <div class="bg-white rounded-2xl shadow-lg p-6 md:p-8 flex flex-col items-center">
          <img src="https://images.unsplash.com/photo-1622988766425-8ecbae9cef6c?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8ZXZlbnRwbGFubmluZ3xlbnwwfHwwfHx8MA%3D%3D" alt="Event Planning" class="w-20 h-20 md:w-28 md:h-28 object-cover rounded-full mb-3 md:mb-4" />
          <h3 class="text-xl md:text-2xl font-semibold text-fuchsia-700 mb-1 md:mb-2">Event Planning</h3>
          <p class="text-gray-600 text-center text-sm md:text-base">We handle every detail, from sound and lighting to scheduling, so you can enjoy your event stress-free.</p>
        </div>
        <div class="bg-white rounded-2xl shadow-lg p-6 md:p-8 flex flex-col items-center">
          <img src="https://images.unsplash.com/photo-1504674900247-0877df9cc836?auto=format&fit=crop&w=400&q=80" alt="Food, Catering & Drink Supplies" class="w-20 h-20 md:w-28 md:h-28 object-cover rounded-full mb-3 md:mb-4" />
          <h3 class="text-xl md:text-2xl font-semibold text-fuchsia-700 mb-1 md:mb-2">Food, Catering & Drink Supplies</h3>
          <p class="text-gray-600 text-center text-sm md:text-base">Delicious food, professional catering, and a wide selection of drinks to keep your guests satisfied and refreshed.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="py-12 md:py-20 px-4 bg-white flex flex-col md:flex-row items-center gap-8 md:gap-10 mx-0 md:mx-25">
    <div class="flex-1 w-full">
      <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-fuchsia-700 mb-3 md:mb-4">Contact Us</h2>
      <form class="space-y-4 md:space-y-6 max-w-md" @submit.prevent="">
        <div>
          <label class="block text-gray-700 font-semibold mb-1 md:mb-2">Name</label>
          <input type="text" class="w-full border border-gray-300 rounded-lg px-3 py-2 md:px-4 md:py-2 focus:outline-none focus:ring-2 focus:ring-fuchsia-400" required />
        </div>
        <div>
          <label class="block text-gray-700 font-semibold mb-1 md:mb-2">Email</label>
          <input type="email" class="w-full border border-gray-300 rounded-lg px-3 py-2 md:px-4 md:py-2 focus:outline-none focus:ring-2 focus:ring-fuchsia-400" required />
        </div>
        <div>
          <label class="block text-gray-700 font-semibold mb-1 md:mb-2">Message</label>
          <textarea class="w-full border border-gray-300 rounded-lg px-3 py-2 md:px-4 md:py-2 focus:outline-none focus:ring-2 focus:ring-fuchsia-400" rows="4" required></textarea>
        </div>
        <button type="submit" class="bg-fuchsia-700 hover:bg-fuchsia-800 text-white font-bold py-2 md:py-3 px-6 md:px-8 rounded-full shadow transition w-full md:w-auto">Send Message</button>
      </form>
    </div>
    <img src="https://images.unsplash.com/photo-1565035010268-a3816f98589a?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fGNvbmNlcnR8ZW58MHx8MHx8fDA%3D" alt="Contact Music Crowd" class="w-full md:w-1/3 rounded-2xl shadow-lg mt-6 md:mt-0" />
  </section>

  <footer class="bg-gradient-to-r from-fuchsia-700 to-pink-600 text-white py-6 md:py-8 mt-8 md:mt-10">
    <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center justify-between px-4 md:px-6 gap-4 md:gap-6">
      <div class="flex items-center gap-2 md:gap-3 mb-3 md:mb-0">
        <img src="./assets/img/logo1.png" alt="SirLarry Entertainment Logo" class="w-14 h-10 md:w-20 md:h-16 rounded-full shadow" />
        <span class="text-lg md:text-2xl font-bold tracking-wide">SirLarry <span class="text-yellow-400 font-semibold">Entertainment</span></span>
      </div>
      <div class="flex gap-4 md:gap-6 text-xl md:text-2xl">
        <a href="#" aria-label="Instagram" class="hover:text-yellow-400 transition"><svg fill="currentColor" viewBox="0 0 24 24" class="w-6 h-6 md:w-7 md:h-7"><path d="M7.75 2h8.5A5.75 5.75 0 0 1 22 7.75v8.5A5.75 5.75 0 0 1 16.25 22h-8.5A5.75 5.75 0 0 1 2 16.25v-8.5A5.75 5.75 0 0 1 7.75 2zm0 1.5A4.25 4.25 0 0 0 3.5 7.75v8.5A4.25 4.25 0 0 0 7.75 20.5h8.5A4.25 4.25 0 0 0 20.5 16.25v-8.5A4.25 4.25 0 0 0 16.25 3.5zm4.25 3.25a5.25 5.25 0 1 1 0 10.5a5.25 5.25 0 0 1 0-10.5zm0 1.5a3.75 3.75 0 1 0 0 7.5a3.75 3.75 0 0 0 0-7.5zm5.13.88a1.13 1.13 0 1 1-2.26 0a1.13 1.13 0 0 1 2.26 0z"/></svg></a>
        <a href="#" aria-label="Twitter" class="hover:text-yellow-400 transition"><svg fill="currentColor" viewBox="0 0 24 24" class="w-6 h-6 md:w-7 md:h-7"><path d="M22.46 5.94c-.8.36-1.67.6-2.58.71a4.48 4.48 0 0 0 1.97-2.48a8.94 8.94 0 0 1-2.83 1.08a4.48 4.48 0 0 0-7.64 4.08A12.74 12.74 0 0 1 3.11 4.6a4.48 4.48 0 0 0 1.39 5.98a4.44 4.44 0 0 1-2.03-.56v.06a4.48 4.48 0 0 0 3.6 4.39a4.5 4.5 0 0 1-2.02.08a4.48 4.48 0 0 0 4.18 3.11A9 9 0 0 1 2 19.54a12.7 12.7 0 0 0 6.88 2.02c8.26 0 12.78-6.84 12.78-12.78c0-.2 0-.39-.01-.58a9.1 9.1 0 0 0 2.23-2.32z"/></svg></a>
        <a href="#" aria-label="Facebook" class="hover:text-yellow-400 transition"><svg fill="currentColor" viewBox="0 0 24 24" class="w-6 h-6 md:w-7 md:h-7"><path d="M22 12c0-5.52-4.48-10-10-10S2 6.48 2 12c0 5 3.66 9.13 8.44 9.88v-6.99H7.9v-2.89h2.54V9.84c0-2.5 1.49-3.89 3.77-3.89c1.09 0 2.23.2 2.23.2v2.45h-1.26c-1.24 0-1.63.77-1.63 1.56v1.87h2.78l-.44 2.89h-2.34v6.99C18.34 21.13 22 17 22 12z"/></svg></a>
      </div>
      <div class="text-center md:text-right text-xs md:text-sm text-gray-200">
        &copy; {{ new Date().getFullYear() }} SirLarry Entertainment. All rights reserved.<br/>
        <span class="text-xs">Made with <span class="text-yellow-400">&#9829;</span> for music lovers.</span>
      </div>
    </div>
  </footer>
</template>
