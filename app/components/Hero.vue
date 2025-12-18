<template>
  <section class="relative w-full">
    <!-- Desktop: Image as background with text overlay -->
    <div class="hidden md:block relative w-full min-h-[600px]">
      <!-- Background Image -->
      <div class="absolute inset-0">
        <NuxtImg
          src="/images/hero.png"
          alt="Business professionals collaborating"
          class="w-full h-full object-cover"
        />
        <!-- Overlay for better text readability -->
        <div class="absolute inset-0 bg-black/10"></div>
      </div>

      <!-- Content Overlay -->
      <div class="relative container mx-auto px-6 lg:px-20 py-24 lg:py-32">
        <div class="max-w-3xl">
          <h1 class="text-5xl font-bold text-gray-800 mb-6 leading-tight">
            PROSPERITY IS BUILT ON
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              INTELLIGENT TECHNOLOGY
            </span>
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              PLATFORMS
            </span>
          </h1>

          <p class="text-2xl text-gray-600 mb-8 leading-relaxed max-w-sm">
            Dijiti builds secure, scalable platforms that empower modern finance
            and enterprise.
          </p>

          <NuxtLink
            to="/contact"
            class="border-2 border-[#1E1B4E] text-[#1E1B4E] px-8 py-3 text-lg rounded-md font-semibold hover:bg-[#1E1B4E] hover:text-white transition-colors duration-300"
          >
            CONTACT US
          </NuxtLink>
        </div>
      </div>
    </div>

    <!-- Mobile: Text first, then image below -->
    <div class="md:hidden">
      <!-- Text Content -->
      <div class="px-6 py-12">
        <h1 class="text-xl font-bold text-gray-800 mb-4 leading-tight">
          PROSPERITY IS BUILT ON
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block"
          >
            INTELLIGENT TECHNOLOGY
          </span>
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block"
          >
            PLATFORMS
          </span>
        </h1>

        <p class="text-lg text-gray-600 mb-6 leading-relaxed">
          Dijiti builds secure, scalable platforms that empower modern finance
          and enterprise.
        </p>

        <NuxtLink
          to="/contact"
          class="border-2 border-[#1E1B4E] text-[#1E1B4E] px-6 py-3 rounded-md text-base font-semibold hover:bg-[#1E1B4E hover:text-white transition-colors duration-300"
        >
          CONTACT US
        </NuxtLink>
      </div>

      <!-- Image Below -->
      <div class="w-full">
        <img
          src="/images/hero-mobile.png"
          alt="Business professionals collaborating"
          class="w-full h-auto object-cover"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
// Component is ready to use - no additional logic needed
</script>

<style scoped>
/* Optional: Add any custom styles here if needed */
</style>
