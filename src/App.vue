<script setup></script>

<template>
  <nav
    class="flex items-center justify-between px-10 bg-gradient-to-r bg-fuchsia-700 to-pink-600 shadow-md sticky top-0 z-50"
  >
    <div class="flex items-center">
      <img src="./assets/img/logo1.png" alt="SirLarry Entertainment Logo" class="w-44 mr-3" />
    </div>
    <ul class="flex gap-8">
      <li><a href="#hero" class="text-white hover:text-yellow-300 transition-colors duration-200 font-medium cursor-pointer">Home</a></li>
      <li><a href="#about" class="text-white hover:text-yellow-300 transition-colors duration-200 font-medium cursor-pointer">About</a></li>
      <li><a href="#services" class="text-white hover:text-yellow-300 transition-colors duration-200 font-medium cursor-pointer">Services</a></li>
      <li><a href="#contact" class="text-white hover:text-yellow-300 transition-colors duration-200 font-medium cursor-pointer">Contact</a></li>
    </ul>
  </nav>

  <!-- Hero Section -->
  <section id="hero" class="relative min-h-[80vh] flex items-center justify-center text-center bg-cover bg-center" style="background-image: url('https://images.unsplash.com/photo-1464983953574-0892a716854b?auto=format&fit=crop&w=1500&q=80');">
    <div class="bg-black bg-opacity-60 p-10 rounded-xl shadow-lg">
      <h1 class="text-5xl md:text-6xl font-extrabold text-white mb-6 drop-shadow-lg">Unleash the <span class="text-yellow-400">Music</span>.<br/>Experience the <span class="text-pink-400">Entertainment</span>.</h1>
      <p class="text-xl text-gray-200 mb-8">SirLarry Entertainment brings the party to life with unforgettable music, events, and vibes.</p>
      <a href="#contact" class="inline-block w-40 h-10 bg-yellow-400 hover:bg-yellow-500 text-fuchsia-900 font-bold rounded-full text-lg shadow transition">Book Us Now</a>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="py-20 px-4 bg-white flex flex-col md:flex-row items-center gap-10">
    <img src="https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?auto=format&fit=crop&w=600&q=80" alt="DJ at work" class="w-full md:w-1/3 rounded-2xl shadow-lg" />
    <div class="max-w-xl">
      <h2 class="text-4xl font-bold text-fuchsia-700 mb-4">About SirLarry Entertainment</h2>
      <p class="text-lg text-gray-700 mb-4">We are passionate about music, events, and creating memories. With years of experience in the entertainment industry, our team delivers top-notch DJ, MC, and event planning services for all occasions. Let us make your next event unforgettable!</p>
      <ul class="list-disc list-inside text-gray-600">
        <li>Professional DJs & MCs</li>
        <li>State-of-the-art sound & lighting</li>
        <li>Custom event experiences</li>
      </ul>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="py-20 px-4 bg-gradient-to-r from-pink-100 to-fuchsia-100">
    <div class="max-w-5xl mx-auto">
      <h2 class="text-4xl font-bold text-center text-fuchsia-700 mb-12">Our Services</h2>
      <div class="grid md:grid-cols-3 gap-10">
        <div class="bg-white rounded-2xl shadow-lg p-8 flex flex-col items-center">
          <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=400&q=80" alt="DJ Service" class="w-28 h-28 object-cover rounded-full mb-4" />
          <h3 class="text-2xl font-semibold text-fuchsia-700 mb-2">DJ Services</h3>
          <p class="text-gray-600 text-center">From weddings to club nights, our DJs keep the dance floor alive with the best beats and mixes.</p>
        </div>
        <div class="bg-white rounded-2xl shadow-lg p-8 flex flex-col items-center">
          <img src="https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?auto=format&fit=crop&w=400&q=80" alt="Live Band" class="w-28 h-28 object-cover rounded-full mb-4" />
          <h3 class="text-2xl font-semibold text-fuchsia-700 mb-2">Live Bands</h3>
          <p class="text-gray-600 text-center">Book talented live bands for a vibrant, energetic atmosphere at your event.</p>
        </div>
        <div class="bg-white rounded-2xl shadow-lg p-8 flex flex-col items-center">
          <img src="https://images.unsplash.com/photo-1465101046530-73398c7f28ca?auto=format&fit=crop&w=400&q=80" alt="Event Planning" class="w-28 h-28 object-cover rounded-full mb-4" />
          <h3 class="text-2xl font-semibold text-fuchsia-700 mb-2">Event Planning</h3>
          <p class="text-gray-600 text-center">We handle every detail, from sound and lighting to scheduling, so you can enjoy your event stress-free.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="py-20 px-4 bg-white flex flex-col md:flex-row items-center gap-10 mx-25">
    <div class="flex-1">
      <h2 class="text-4xl font-bold text-fuchsia-700 mb-4">Contact Us</h2>
      <form class="space-y-6 max-w-md" @submit.prevent="">
        <div>
          <label class="block text-gray-700 font-semibold mb-2">Name</label>
          <input type="text" class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-fuchsia-400" required />
        </div>
        <div>
          <label class="block text-gray-700 font-semibold mb-2">Email</label>
          <input type="email" class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-fuchsia-400" required />
        </div>
        <div>
          <label class="block text-gray-700 font-semibold mb-2">Message</label>
          <textarea class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-fuchsia-400" rows="4" required></textarea>
        </div>
        <button type="submit" class="bg-fuchsia-700 hover:bg-fuchsia-800 text-white font-bold py-3 px-8 rounded-full shadow transition">Send Message</button>
      </form>
    </div>
    <img src="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=600&q=80" alt="Contact Music Crowd" class="w-full md:w-1/3 rounded-2xl shadow-lg mt-10 md:mt-0" />
  </section>

  <footer class="bg-gradient-to-r from-fuchsia-700 to-pink-600 text-white py-8 mt-10">
    <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center justify-between px-6 gap-6">
      <div class="flex items-center gap-3 mb-4 md:mb-0">
        <img src="./assets/img/logo1.png" alt="SirLarry Entertainment Logo" class="w-20 h-16 rounded-full shadow" />
        <span class="text-2xl font-bold tracking-wide">SirLarry <span class="text-yellow-400 font-semibold">Entertainment</span></span>
      </div>
      <div class="flex gap-6 text-2xl">
        <a href="#" aria-label="Instagram" class="hover:text-yellow-400 transition"><svg fill="currentColor" viewBox="0 0 24 24" class="w-7 h-7"><path d="M7.75 2h8.5A5.75 5.75 0 0 1 22 7.75v8.5A5.75 5.75 0 0 1 16.25 22h-8.5A5.75 5.75 0 0 1 2 16.25v-8.5A5.75 5.75 0 0 1 7.75 2zm0 1.5A4.25 4.25 0 0 0 3.5 7.75v8.5A4.25 4.25 0 0 0 7.75 20.5h8.5A4.25 4.25 0 0 0 20.5 16.25v-8.5A4.25 4.25 0 0 0 16.25 3.5zm4.25 3.25a5.25 5.25 0 1 1 0 10.5a5.25 5.25 0 0 1 0-10.5zm0 1.5a3.75 3.75 0 1 0 0 7.5a3.75 3.75 0 0 0 0-7.5zm5.13.88a1.13 1.13 0 1 1-2.26 0a1.13 1.13 0 0 1 2.26 0z"/></svg></a>
        <a href="#" aria-label="Twitter" class="hover:text-yellow-400 transition"><svg fill="currentColor" viewBox="0 0 24 24" class="w-7 h-7"><path d="M22.46 5.94c-.8.36-1.67.6-2.58.71a4.48 4.48 0 0 0 1.97-2.48a8.94 8.94 0 0 1-2.83 1.08a4.48 4.48 0 0 0-7.64 4.08A12.74 12.74 0 0 1 3.11 4.6a4.48 4.48 0 0 0 1.39 5.98a4.44 4.44 0 0 1-2.03-.56v.06a4.48 4.48 0 0 0 3.6 4.39a4.5 4.5 0 0 1-2.02.08a4.48 4.48 0 0 0 4.18 3.11A9 9 0 0 1 2 19.54a12.7 12.7 0 0 0 6.88 2.02c8.26 0 12.78-6.84 12.78-12.78c0-.2 0-.39-.01-.58a9.1 9.1 0 0 0 2.23-2.32z"/></svg></a>
        <a href="#" aria-label="Facebook" class="hover:text-yellow-400 transition"><svg fill="currentColor" viewBox="0 0 24 24" class="w-7 h-7"><path d="M22 12c0-5.52-4.48-10-10-10S2 6.48 2 12c0 5 3.66 9.13 8.44 9.88v-6.99H7.9v-2.89h2.54V9.84c0-2.5 1.49-3.89 3.77-3.89c1.09 0 2.23.2 2.23.2v2.45h-1.26c-1.24 0-1.63.77-1.63 1.56v1.87h2.78l-.44 2.89h-2.34v6.99C18.34 21.13 22 17 22 12z"/></svg></a>
      </div>
      <div class="text-center md:text-right text-sm text-gray-200">
        &copy; {{ new Date().getFullYear() }} SirLarry Entertainment. All rights reserved.<br/>
        <span class="text-xs">Made with <span class="text-yellow-400">&#9829;</span> for music lovers.</span>
      </div>
    </div>
  </footer>
</template>
