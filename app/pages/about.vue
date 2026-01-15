<template>
  <section class="relative w-full">
    <!-- Desktop: Image as background with text overlay -->
    <div class="hidden md:block relative w-full h-screen">
      <!-- Background Image -->
      <div class="absolute inset-0">
        <NuxtImg
          src="/images/about-hero.png"
          alt="Business professionals collaborating"
          class="w-full h-full object-cover"
        />
        <!-- Overlay for better text readability -->
        <div class="absolute inset-0 bg-black/10"></div>
      </div>

      <!-- Content Overlay -->
      <div
        class="relative container mx-auto px-6 lg:px-20 h-full flex items-center [@media(max-height:650px)]:items-center"
      >
        <div class="max-w-3xl">
          <h1
            class="text-5xl font-bold text-gray-800 mb-6 leading-tight uppercase"
          >
            60 Years of Expertise
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              The Foundation of
            </span>
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              Flawless Execution
            </span>
          </h1>

          <p class="text-2xl text-gray-600 mb-8 leading-relaxed max-w-sm">
            As a proud, Level 2 BBBEE-compliant South African firm, we deliver
            strategic value through global networks.
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
        <h1
          class="text-2xl font-bold text-gray-800 mb-4 leading-tight uppercase"
        >
          60 Years of Expertise
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block uppercase"
          >
            The Foundation of
          </span>
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block uppercase"
          >
            Flawless Execution
          </span>
        </h1>

        <p class="text-lg text-gray-600 mb-6 leading-relaxed">
          As a proud, Level 2 BBBEE-compliant South African firm, we deliver
          strategic value through global networks.
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
          src="/images/about-mobile-header.png"
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
          TRANSFORMING BUSINESS, EMPOWERING HUMANITY
        </h3>
        <p
          class="leading-tight opacity-0 my-5 font-light"
          data-anim="fade"
          data-delay="0.2s"
        >
          Dijiti Solutions is a global innovation group that designs secure
          platforms to connect people, data, and enterprises, bridging the gap
          between technology and human progress.
        </p>

        <p
          class="leading-tight opacity-0 font-light"
          data-anim="fade"
          data-delay="0.6s"
        >
          As expert digital platform developers, our mission is to deliver
          solutions that are intelligent, scalable, and fundamentally
          transformative.
        </p>
      </div>
    </div>
  </section>

  <FoundationSection />

  <LeadershipSection />

  <!-- <section class="bg-gray-100">
    <div
      class="max-w-4xl text-gray-600 mx-auto py-16 space-y-6 text-2xl md:text-[28px] text-center lg:px-0 px-6"
    >
      <div>
        <h3
          class="border border-gray-500 py-2 px-2 mb-8 md:text-4xl text-2xl font-light"
        >
          OUR COMMITMENT
        </h3>
        <h4 class="text-2xl font-semibold mb-1">Proudly South African:</h4>
        <p
          class="leading-tight opacity-0 font-light"
          data-anim="fade"
          data-delay="0.2s"
        >
          We manage the South African team, providing the scope of work,
          overseeing project execution, and delivering high-quality, impactful
          solutions.
        </p>
        <h4 class="text-2xl font-semibold mt-5 mb-1">
          Level 2 BBBEE Compliant:
        </h4>
        <p
          class="leading-tight opacity-0 font-light"
          data-anim="fade"
          data-delay="0.6s"
        >
          Our 40% ownership in Word of Mouth (smart lead generation) expands our
          reach, boosts economic growth, and creates business opportunities for
          everyday South Africans.
        </p>
      </div>
    </div>
  </section> -->

  <CompaniesSection />

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
