<template>
  <section class="relative w-full">
    <!-- Desktop: Image as background with text overlay -->
    <div class="hidden md:block relative w-full min-h-[600px]">
      <!-- Background Image -->
      <div class="absolute inset-0">
        <NuxtImg
          src="/images/Desktop-Resoruces.png"
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
            THOUGHT LEADERSHIP
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              THAT DRIVES PROGRESS
            </span>
          </h1>

          <p class="text-2xl text-gray-600 mb-8 leading-relaxed max-w-sm">
            Stay informed with expert analysis on strategic consulting,
            financial services, and enterprise technology.
          </p>

          <button
            class="border-2 border-[#1E1B4E] text-[#1E1B4E] px-8 py-3 text-lg rounded-md font-semibold hover:bg-[#1E1B4E] hover:text-white transition-colors duration-300"
          >
            CONTACT US
          </button>
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
          THOUGHT LEADERSHIP
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block uppercase"
          >
            HAT DRIVES PROGRESS.
          </span>
        </h1>

        <p class="text-lg text-gray-600 mb-6 leading-relaxed">
          Stay informed with expert analysis on strategic consulting, financial
          services, and enterprise technology.
        </p>

        <button
          class="border-2 border-[#1E1B4E] text-[#1E1B4E] px-6 py-3 text-base font-semibold rounded-md hover:bg-[#1E1B4E hover:text-white transition-colors duration-300"
        >
          CONTACT US
        </button>
      </div>

      <!-- Image Below -->
      <div class="w-full">
        <NuxtImg
          src="/images/Mobile-Resoruces.png"
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
          class="border border-white py-2 px-2 mb-4 md:text-4xl text-2xl font-light w-fit mx-auto"
        >
          RESOURCES: BLOG, INSIGHTS, INDUSTRY NEWS
        </h3>
        <p
          class="leading-tight opacity-0 my-5 font-light"
          data-anim="fade"
          data-delay="0.2s"
        >
          Discover expert analysis, strategic insights, and global perspectives
          that inspire progress and compliance across finance and industry.
        </p>
      </div>
    </div>
  </section>

  <section>
    <div
      class="max-w-7xl mx-auto flex md:flex-row flex-col gap-8 justify-center pb-8 py-8 px-4"
    >
      <div class="bg-white rounded-lg max-w-sm md:max-w-72">
        <div>
          <div class="pr-6">
            <!-- Blog Title -->
            <h3
              class="md:text-3xl text-3xl font-bold text-gray-900 mb-2 uppercase"
            >
              FEATURED ARTICLE BLOCK
            </h3>

            <!-- Publish Date and Category -->
            <p class="text-sm text-gray-500 mb-2">
              01 December, 2025 | Fintech
            </p>

            <div class="w-16 h-[2px] bg-gray-900"></div>

            <!-- Description -->
            <p
              class="text-gray-700 md:text-2xl text-lg leading-relaxed mb-6 mt-2"
            >
              Top article showcased with feature image, excerpt, and Read More
              link.
            </p>

            <!-- Read Article Button -->
            <button
              class="text-gray-500 border border-gray-500 font-semibold py-2 px-6 transition-colors duration-300"
            >
              READ ARTICLE >
            </button>
          </div>
        </div>
      </div>
      <div class="relative z-[99999]">
        <!-- Featured Image -->
        <div class="w-full md:h-72 b">
          <img
            src="/images/Featured.png"
            alt="Blog post image"
            class="w-full h-full object-cover relative z-[9999]"
          />
        </div>
      </div>
    </div>
  </section>

  <section class="h-full">
    <div class="relative bg-[#1E1B3B]">
      <!-- <div
        class="absolute top-0 left-0 right-0 h-32 bg-[#333841] -skew-y-3 origin-top-left transform"
      ></div> -->

      <!-- Background color -->
      <div class="max-w-7xl mx-auto">
        <!-- Title -->
        <div class="flex items-center justify-center">
          <div
            class="flex items-center gap-3 p-6 rounded-lg z-10 mt-2 overflow-x-auto whitespace-nowrap snap-x snap-mandatory md:justify-center justify-start w-full"
          >
            <!-- ALL ARTICLES -->
            <button
              class="px-6 py-2 text-lg font-medium text-gray-900 bg-white rounded-full hover:bg-gray-100 transition-colors md:min-w-44 snap-start"
            >
              ALL ARTICLES
            </button>

            <!-- FINTECH -->
            <button
              class="px-6 py-2 text-lg font-medium text-gray-300 bg-transparent border border-gray-300 rounded-full hover:bg-white hover:text-gray-900 transition-colors md:min-w-44 snap-start"
            >
              BLOGS
            </button>

            <!-- AI -->
            <button
              class="px-6 py-2 text-lg font-medium text-gray-300 bg-transparent border border-gray-300 rounded-full hover:bg-white hover:text-gray-900 transition-colors md:min-w-44 snap-start"
            >
              INSIGHTS
            </button>

            <!-- DATA -->
            <button
              class="px-6 py-2 text-lg font-medium text-gray-300 bg-transparent border border-gray-300 rounded-full hover:bg-white hover:text-gray-900 transition-colors md:min-w-44 snap-start"
            >
              INDUSTRY
            </button>

            <!-- CONSTRUCTION -->
            <button
              class="px-6 py-2 text-lg font-medium text-gray-300 bg-transparent border border-gray-300 rounded-full hover:bg-white hover:text-gray-900 transition-colors md:min-w-44 snap-start"
            >
              NEWS
            </button>
          </div>
        </div>

        <!-- Cards Container -->
        <div class="px-4 pb-16 relative z-50">
          <div
            class="flex flex-col md:flex-row gap-5 md:gap-10 justify-center max-w-6xl mx-auto w-full"
          >
            <!-- Blog Article 1 -->
            <div
              class="bg-white rounded-lg overflow-hidden shadow-xl md:max-w-xs w-full"
            >
              <div>
                <!-- Featured Image Placeholder -->
                <div class="w-full h-full bg-gray-300">
                  <img
                    src="/images/Article.png"
                    alt="Blog post image"
                    class="object-cover h-48 w-full"
                  />
                </div>

                <div class="p-6">
                  <!-- Blog Title -->
                  <h3 class="text-xl font-bold text-gray-900 mb-2 uppercase">
                    A BLOG POST ARTICLE TITLE
                  </h3>

                  <!-- Publish Date and Category -->
                  <p class="text-sm text-gray-500 mb-4">
                    01 December, 2025 | Fintech
                  </p>

                  <!-- Description -->
                  <p class="text-gray-700 text-base leading-relaxed mb-6">
                    Article block showcased with featured image, a very short
                    excerpt, and Read article link.
                  </p>

                  <!-- Read Article Button -->
                  <button
                    class="text-gray-500 border border-gray-500 font-semibold py-2 px-6 rounded-md transition-colors duration-300 hover:bg-[#1E1B4E] hover:text-white"
                  >
                    READ ARTICLE >
                  </button>
                </div>
              </div>
            </div>

            <!-- Blog Article 2 -->
            <div
              class="bg-white rounded-lg overflow-hidden shadow-xl md:max-w-xs w-full"
            >
              <div>
                <!-- Featured Image Placeholder -->
                <div class="w-full h-full bg-gray-300">
                  <img
                    src="/images/Article.png"
                    alt="Blog post image"
                    class="object-cover h-48 w-full"
                  />
                </div>

                <div class="p-6">
                  <!-- Blog Title -->
                  <h3 class="text-xl font-bold text-gray-900 mb-2 uppercase">
                    A BLOG POST ARTICLE TITLE
                  </h3>

                  <!-- Publish Date and Category -->
                  <p class="text-sm text-gray-500 mb-4">
                    01 December, 2025 | Fintech
                  </p>

                  <!-- Description -->
                  <p class="text-gray-700 text-base leading-relaxed mb-6">
                    Article block showcased with featured image, a very short
                    excerpt, and Read article link.
                  </p>

                  <!-- Read Article Button -->
                  <button
                    class="text-gray-500 border border-gray-500 font-semibold py-2 px-6 rounded-md transition-colors duration-300 hover:bg-[#1E1B4E] hover:text-white"
                  >
                    READ ARTICLE >
                  </button>
                </div>
              </div>
            </div>

            <!-- Blog Article 3 -->
            <div
              class="bg-white rounded-lg overflow-hidden shadow-xl md:max-w-xs w-full"
            >
              <div>
                <!-- Featured Image Placeholder -->
                <div class="w-full h-full bg-gray-300">
                  <img
                    src="/images/Article.png"
                    alt="Blog post image"
                    class="object-cover h-48 w-full"
                  />
                </div>

                <div class="p-6">
                  <!-- Blog Title -->
                  <h3 class="text-xl font-bold text-gray-900 mb-2 uppercase">
                    A BLOG POST ARTICLE TITLE
                  </h3>

                  <!-- Publish Date and Category -->
                  <p class="text-sm text-gray-500 mb-4">
                    01 December, 2025 | Fintech
                  </p>

                  <!-- Description -->
                  <p class="text-gray-700 text-base leading-relaxed mb-6">
                    Article block showcased with featured image, a very short
                    excerpt, and Read article link.
                  </p>

                  <!-- Read Article Button -->
                  <button
                    class="text-gray-500 border border-gray-500 font-semibold py-2 px-6 rounded-md transition-colors duration-300 hover:bg-[#1E1B4E] hover:text-white"
                  >
                    READ ARTICLE >
                  </button>
                </div>
              </div>
            </div>
          </div>

          <div
            class="flex flex-col md:flex-row gap-5 md:gap-10 justify-center max-w-6xl mx-auto w-full mt-5 md:mt-10"
          >
            <!-- Blog Article 1 -->
            <div
              class="bg-white rounded-lg overflow-hidden shadow-xl md:max-w-xs w-full"
            >
              <div>
                <!-- Featured Image Placeholder -->
                <div class="w-full h-full bg-gray-300">
                  <img
                    src="/images/Article.png"
                    alt="Blog post image"
                    class="object-cover h-48 w-full"
                  />
                </div>

                <div class="p-6">
                  <!-- Blog Title -->
                  <h3 class="text-xl font-bold text-gray-900 mb-2 uppercase">
                    A BLOG POST ARTICLE TITLE
                  </h3>

                  <!-- Publish Date and Category -->
                  <p class="text-sm text-gray-500 mb-4">
                    01 December, 2025 | Fintech
                  </p>

                  <!-- Description -->
                  <p class="text-gray-700 text-base leading-relaxed mb-6">
                    Article block showcased with featured image, a very short
                    excerpt, and Read article link.
                  </p>

                  <!-- Read Article Button -->
                  <button
                    class="text-gray-500 border border-gray-500 font-semibold py-2 px-6 rounded-md transition-colors duration-300 hover:bg-[#1E1B4E] hover:text-white"
                  >
                    READ ARTICLE >
                  </button>
                </div>
              </div>
            </div>

            <!-- Blog Article 2 -->
            <div
              class="bg-white rounded-lg overflow-hidden shadow-xl md:max-w-xs w-full"
            >
              <div>
                <!-- Featured Image Placeholder -->
                <div class="w-full h-full bg-gray-300">
                  <img
                    src="/images/Article.png"
                    alt="Blog post image"
                    class="object-cover h-48 w-full"
                  />
                </div>

                <div class="p-6">
                  <!-- Blog Title -->
                  <h3 class="text-xl font-bold text-gray-900 mb-2 uppercase">
                    A BLOG POST ARTICLE TITLE
                  </h3>

                  <!-- Publish Date and Category -->
                  <p class="text-sm text-gray-500 mb-4">
                    01 December, 2025 | Fintech
                  </p>

                  <!-- Description -->
                  <p class="text-gray-700 text-base leading-relaxed mb-6">
                    Article block showcased with featured image, a very short
                    excerpt, and Read article link.
                  </p>

                  <!-- Read Article Button -->
                  <button
                    class="text-gray-500 border border-gray-500 font-semibold py-2 px-6 rounded-md transition-colors duration-300 hover:bg-[#1E1B4E] hover:text-white"
                  >
                    READ ARTICLE >
                  </button>
                </div>
              </div>
            </div>

            <!-- Blog Article 3 -->
            <div
              class="bg-white rounded-lg overflow-hidden shadow-xl md:max-w-xs w-full"
            >
              <div>
                <!-- Featured Image Placeholder -->
                <div class="w-full h-full bg-gray-300">
                  <img
                    src="/images/Article.png"
                    alt="Blog post image"
                    class="object-cover h-48 w-full"
                  />
                </div>

                <div class="p-6">
                  <!-- Blog Title -->
                  <h3 class="text-xl font-bold text-gray-900 mb-2 uppercase">
                    A BLOG POST ARTICLE TITLE
                  </h3>

                  <!-- Publish Date and Category -->
                  <p class="text-sm text-gray-500 mb-4">
                    01 December, 2025 | Fintech
                  </p>

                  <!-- Description -->
                  <p class="text-gray-700 text-base leading-relaxed mb-6">
                    Article block showcased with featured image, a very short
                    excerpt, and Read article link.
                  </p>

                  <!-- Read Article Button -->
                  <button
                    class="text-gray-500 border border-gray-500 font-semibold py-2 px-6 rounded-md transition-colors duration-300 hover:bg-[#1E1B4E] hover:text-white"
                  >
                    READ ARTICLE >
                  </button>
                </div>
              </div>
            </div>
          </div>
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
