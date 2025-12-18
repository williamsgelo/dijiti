<template>
  <section class="relative w-full">
    <!-- Desktop: Image as background with text overlay -->
    <div class="hidden md:block relative w-full min-h-[600px]">
      <!-- Background Image -->
      <div class="absolute inset-0">
        <NuxtImg
          src="/images/Desktop-Our-Work.png"
          alt="Business professionals collaborating"
          class="w-full h-full object-cover"
        />
        <!-- Overlay for better text readability -->
        <div class="absolute inset-0 bg-black/10"></div>
      </div>

      <!-- Content Overlay -->
      <div class="relative container mx-auto px-6 lg:px-20 py-24 lg:py-32">
        <div class="max-w-3xl">
          <h1
            class="text-5xl font-bold text-gray-800 mb-6 leading-tight uppercase"
          >
            RESULTS DELIVERED
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              STRATEGIC EXECUTION
            </span>
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              IN ACTION
            </span>
          </h1>

          <p class="text-2xl text-gray-600 mb-8 leading-relaxed max-w-sm">
            Review our portfolio of high-impact projects and see how our
            expertise solves complex challenges for global enterprises.
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
      <div class="bg-gray-100 px-6 py-12">
        <h1
          class="text-2xl font-bold text-gray-800 mb-4 leading-tight uppercase"
        >
          RESULTS DELIVERED
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block uppercase"
          >
            STRATEGIC EXECUTION
          </span>
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block uppercase"
          >
            IN ACTION
          </span>
        </h1>

        <p class="text-lg text-gray-600 mb-6 leading-relaxed">
          Review our portfolio of high-impact projects and see how our expertise
          solves complex challenges for global enterprises.
        </p>

        <NuxtLink
          to="/contact"
          class="border-2 border-[#1E1B4E] text-[#1E1B4E] px-6 py-3 text-base rounded-md font-semibold hover:bg-[#1E1B4E hover:text-white transition-colors duration-300"
        >
          CONTACT US
        </NuxtLink>
      </div>

      <!-- Image Below -->
      <div class="w-full">
        <NuxtImg
          src="/images/Mobile-Our-Work.png"
          alt="Business professionals collaborating"
          class="w-full h-auto object-cover"
        />
      </div>
    </div>
  </section>

  <section class="relative overflow-hidden">
    <!-- Background image -->
    <NuxtImg
      src="/images/about-gradient.png"
      alt="Digiti background"
      class="absolute inset-0 w-full h-full object-cover"
    />

    <!-- Content -->
    <div
      class="relative max-w-4xl text-white mx-auto py-16 space-y-6 text-2xl md:text-[28px] text-center lg:px-0 px-6"
    >
      <div>
        <h3
          class="border border-white py-2 px-2 mb-4 text-2xl font-light w-fit mx-auto"
        >
          CASE STUDIES IN DIGITAL TRANSFORMATION
        </h3>
        <p
          class="leading-tight opacity-0 my-5 font-light"
          data-anim="fade"
          data-delay="0.2s"
        >
          Explore our portfolio of high-impact projects. See how Dijiti delivers
          measurable results in digital transformation, compliance, and
          enterprise efficiency.
        </p>
      </div>
    </div>
  </section>

  <section class="max-w-7xl mx-auto px-4 py-16">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <!-- Card -->
      <div class="overflow-hidden shadow-lg border">
        <img
          src="/images/Project-Our-Work.png"
          alt="Project image"
          class="w-full h-56 md:h-96 object-cover"
        />
        <div
          class="bg-gradient-to-r from-indigo-900 to-purple-600 py-6 hover:bg-gradient-to-r hover:from-purple-600 hover:to-indigo-900 transition-all duration-300 cursor-pointer"
        >
          <p class="text-center text-white text-xl tracking-widest">PROJECT</p>
        </div>
      </div>

      <!-- Duplicate cards (x6 total) -->
      <div class="overflow-hidden shadow-lg border">
        <img
          src="/images/Project-Our-Work.png"
          alt="Project image"
          class="w-full h-56 md:h-96 object-cover"
        />
        <div
          class="bg-gradient-to-r from-indigo-900 to-purple-600 py-6 hover:bg-gradient-to-r hover:from-purple-600 hover:to-indigo-900 transition-all duration-300 cursor-pointer"
        >
          <p class="text-center text-white text-xl tracking-widest">PROJECT</p>
        </div>
      </div>

      <div class="overflow-hidden shadow-lg border">
        <img
          src="/images/Project-Our-Work.png"
          alt="Project image"
          class="w-full h-56 md:h-96 object-cover"
        />
        <div
          class="bg-gradient-to-r from-indigo-900 to-purple-600 py-6 hover:bg-gradient-to-r hover:from-purple-600 hover:to-indigo-900 transition-all duration-300 cursor-pointer"
        >
          <p class="text-center text-white text-xl tracking-widest">PROJECT</p>
        </div>
      </div>

      <div class="overflow-hidden shadow-lg border">
        <img
          src="/images/Project-Our-Work.png"
          alt="Project image"
          class="w-full h-56 md:h-96 object-cover"
        />
        <div
          class="bg-gradient-to-r from-indigo-900 to-purple-600 py-6 hover:bg-gradient-to-r hover:from-purple-600 hover:to-indigo-900 transition-all duration-300 cursor-pointer"
        >
          <p class="text-center text-white text-xl tracking-widest">PROJECT</p>
        </div>
      </div>

      <div class="overflow-hidden shadow-lg border">
        <img
          src="/images/Project-Our-Work.png"
          alt="Project image"
          class="w-full h-56 md:h-96 object-cover"
        />
        <div
          class="bg-gradient-to-r from-indigo-900 to-purple-600 py-6 hover:bg-gradient-to-r hover:from-purple-600 hover:to-indigo-900 transition-all duration-300 cursor-pointer"
        >
          <p class="text-center text-white text-xl tracking-widest">PROJECT</p>
        </div>
      </div>

      <div class="overflow-hidden shadow-lg border">
        <img
          src="/images/Project-Our-Work.png"
          alt="Project image"
          class="w-full h-56 md:h-96 object-cover"
        />
        <div
          class="bg-gradient-to-r from-indigo-900 to-purple-600 py-6 hover:bg-gradient-to-r hover:from-purple-600 hover:to-indigo-900 transition-all duration-300 cursor-pointer"
        >
          <p class="text-center text-white text-xl tracking-widest">PROJECT</p>
        </div>
      </div>
    </div>
  </section>

  <div class="floating-button">
    <LazyBackToTop />
  </div>
</template>

<script setup>
import { onMounted } from "vue";

onMounted(() => {
  const prefersReduced = window.matchMedia(
    "(prefers-reduced-motion: reduce)"
  ).matches;
  const elems = Array.from(document.querySelectorAll("[data-anim]"));

  if (prefersReduced) {
    elems.forEach((el) => {
      el.style.opacity = "1";
    });
    return;
  }

  const observer = new IntersectionObserver(
    (entries, obs) => {
      entries.forEach((entry) => {
        if (!entry.isIntersecting) return;
        const el = entry.target;
        const delay = el.dataset.delay || "0s";
        el.style.animationDelay = delay;

        el.classList.add("animate-fadeIn");
        obs.unobserve(el);
      });
    },
    { threshold: 0.18, rootMargin: "0px 0px -10% 0px" }
  );

  elems.forEach((el) => {
    el.style.opacity = "0";
    observer.observe(el);
  });
});
</script>

<style scoped>
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
.animate-fadeIn {
  animation: fadeIn 800ms ease-out forwards;
}
</style>
