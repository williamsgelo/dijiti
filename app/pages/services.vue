<template>
  <section class="relative w-full">
    <!-- Desktop: Image as background with text overlay -->
    <div class="hidden md:block relative w-full h-screen">
      <!-- Background Image -->
      <div class="absolute inset-0">
        <NuxtImg
          src="/images/Desktop-Services.png"
          alt="Business professionals collaborating"
          class="w-full h-full object-cover"
        />
        <!-- Overlay for better text readability -->
        <div class="absolute inset-0 bg-black/10"></div>
      </div>

      <!-- Content Overlay -->
      <div
        class="relative container mx-auto px-6 lg:px-20 h-full flex items-center short-height-start"
      >
        <div class="max-w-3xl">
          <h1
            class="text-5xl font-bold text-gray-800 mb-6 leading-tight uppercase"
          >
            VALUE-DRIVEN DELIVERY
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              COMPLIANCE, OPTIMISATION,
            </span>
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              AND PREMIUM ACCESS
            </span>
          </h1>

          <p class="text-2xl text-gray-600 mb-8 leading-relaxed max-w-sm">
            We leverage deep industry knowledge to empower your business to
            optimise operations and ensure regulatory compliance.
          </p>

          <NuxtLink
            to="/contact"
            class="border-2 border-[#1E1B4E] text-[#1E1B4E] px-8 py-3 rounded-md text-lg font-semibold hover:bg-[#1E1B4E] hover:text-white transition-colors duration-300"
          >
            SCHEDULE A STRATEGY SESSION
          </NuxtLink>
        </div>
      </div>
    </div>

    <!-- Mobile: Text first, then image below -->
    <div class="md:hidden">
      <!-- Text Content -->
      <div class="bg-gray-100 px-6 py-12">
        <h1
          class="text-xl font-bold text-gray-800 mb-4 leading-tight uppercase"
        >
          VALUE-DRIVEN DELIVERY
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block uppercase"
          >
            COMPLIANCE, OPTIMISATION,
          </span>
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block uppercase"
          >
            AND PREMIUM ACCESS
          </span>
        </h1>

        <p class="text-lg text-gray-600 mb-6 leading-relaxed">
          We leverage deep industry knowledge to empower your business to
          optimise operations and ensure regulatory compliance.
        </p>

        <NuxtLink
          to="/contact"
          class="border-2 border-[#1E1B4E] text-[#1E1B4E] px-6 py-3 text-base rounded-md font-semibold hover:bg-[#1E1B4E hover:text-white transition-colors duration-300"
        >
          SCHEDULE A STRATEGY SESSION
        </NuxtLink>
      </div>

      <!-- Image Below -->
      <div class="w-full">
        <NuxtImg
          src="/images/Mobile-Services.png"
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
        <h3 class="border border-white py-2 px-2 mb-4 text-2xl font-light">
          VALUE-DRIVEN DELIVERY: COMPLIANCE, OPTIMISATION, AND PREMIUM ACCESS
        </h3>
        <p
          class="leading-tight opacity-0 my-5 font-light"
          data-anim="fade"
          data-delay="0.2s"
        >
          Dijiti delivers comprehensive services designed to help organisations
          meet critical regulatory demands, modernise, and scale. From strategy
          to execution, we empower clients with the tools and expertise to
          thrive in the complex digital economy.
        </p>
      </div>
    </div>
  </section>

  <section class="bg-gray-100">
    <!-- Content -->
    <div
      class="text-[#1e1b4e] mx-auto py-16 space-y-6 text-2xl md:text-[28px] text-center lg:px-0 px-6"
    >
      <div>
        <h3
          class="border border-[#1e1b4e] py-3 px-3 mb-12 md:text-5xl text-2xl font-light w-fit mx-auto"
        >
          CORE SERVICES
        </h3>
      </div>

      <div class="max-w-7xl mx-auto md:px-5">
        <div class="grid md:grid-cols-2 gap-x-16 gap-y-12">
          <!-- Service 1 -->
          <div class="flex items-center gap-6">
            <div class="flex-shrink-0 flex items-center justify-center">
              <img
                src="/images/Custom-software-development.svg"
                alt="Custom software"
                class="w-28 md:h-28 h-20"
              />
            </div>
            <h3
              class="md:text-3xl text-2xl text-gray-600 italic font-light text-start"
            >
              Custom software<br />development
            </h3>
          </div>

          <!-- Service 2 -->
          <div class="flex items-center gap-6">
            <div class="flex-shrink-0 flex items-center justify-center">
              <img
                src="/images/AI-consulting.svg"
                alt="AI consulting"
                class="w-28 md:h-28 h-20"
              />
            </div>
            <h3
              class="md:text-3xl text-2xl text-gray-600 italic font-light text-start"
            >
              AI consulting and<br />implementation
            </h3>
          </div>

          <!-- Service 3 -->
          <div class="flex items-center gap-6">
            <div class="flex-shrink-0 flex items-center justify-center">
              <img
                src="/images/Fintech-platforms.svg"
                alt="Fintech"
                class="w-28 md:h-28 h-20"
              />
            </div>
            <h3
              class="md:text-3xl text-2xl text-gray-600 italic font-light text-start"
            >
              Fintech platforms
            </h3>
          </div>

          <!-- Service 4 -->
          <div class="flex items-center gap-6">
            <div class="flex-shrink-0 flex items-center justify-center">
              <img
                src="/images/Resource-management.svg"
                alt="Resource management"
                class="w-28 md:h-28 h-20"
              />
            </div>
            <h3
              class="md:text-3xl text-2xl text-gray-600 italic font-light text-start"
            >
              Resource management<br />platforms
            </h3>
          </div>

          <!-- Service 5 -->
          <div class="flex items-center gap-6">
            <div class="flex-shrink-0 flex items-center justify-center">
              <img
                src="/images/Management-workflow.svg"
                alt="Workflow automation"
                class="w-28 md:h-28 h-20"
              />
            </div>
            <h3
              class="md:text-3xl text-2xl text-gray-600 italic font-light text-start"
            >
              Management and workflow<br />automation platforms
            </h3>
          </div>

          <!-- Service 6 -->
          <div class="flex items-center gap-6">
            <div class="flex-shrink-0 flex items-center justify-center">
              <img
                src="/images/Technology-consulting.svg"
                alt="Technology consulting"
                class="w-28 md:h-28 h-20"
              />
            </div>
            <h3
              class="md:text-3xl text-2xl text-gray-600 italic font-light text-start"
            >
              Technology consulting<br />and strategy
            </h3>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div
      class="max-w-4xl text-gray-600 mx-auto py-16 space-y-6 text-2xl md:text-[28px] text-center lg:px-0 px-6"
    >
      <div>
        <h3
          class="border border-gray-500 py-2 px-2 mb-8 md:text-4xl text-2xl font-light uppercase w-fit mx-auto"
        >
          Expert Consulting
        </h3>
        <p
          class="leading-tight opacity-0 font-light text-2xl"
          data-anim="fade"
          data-delay="0.2s"
        >
          We leverage our deep industry knowledge and highly skilled human
          talent to deliver high-quality, impactful solutions. We empower
          businesses to
          <strong class="font-semibold">
            optimise operations, ensure regulatory compliance, and drive
            transformative growth in the financial services sector.
          </strong>
        </p>
        <h4 class="text-2xl font-semibold mt-5 mb-1 text-[#7c3aed]">
          Strategic Digital Advisory and Project Planning
        </h4>
        <p
          class="leading-tight opacity-0 font-light text-2xl"
          data-anim="fade"
          data-delay="0.6s"
        >
          We offer guidance built on over 60 years of combined global industry
          insight.
        </p>
        <h4 class="text-2xl font-semibold mt-5 mb-1 text-[#7c3aed]">
          System Integration
        </h4>
        <p
          class="leading-tight opacity-0 font-light text-2xl"
          data-anim="fade"
          data-delay="0.6s"
        >
          Linking legacy and cloud infrastructure for seamless efficiency and
          core system stability.
        </p>
        <h4 class="text-2xl font-semibold mt-5 mb-1 text-[#7c3aed]">
          Digital Transformation Strategy
        </h4>
        <p
          class="leading-tight opacity-0 font-light text-2xl"
          data-anim="fade"
          data-delay="0.6s"
        >
          Developing clear, actionable roadmaps for modern business evolution.
        </p>
      </div>
    </div>
  </section>

  <section>
    <div class="relative overflow-hidden">
      <!-- Background image -->
      <NuxtImg
        src="/images/about-gradient.png"
        alt="Digiti background"
        class="absolute inset-0 w-full h-full object-cover"
      />

      <!-- Content -->
      <div
        class="relative max-w-4xl text-white mx-auto pt-16 pb-32 space-y-6 text-2xl md:text-[28px] text-center lg:px-0 px-6"
      >
        <div>
          <h3
            class="border border-white py-2 px-2 mb-4 md:text-4xl text-2xl font-light w-fit mx-auto"
          >
            RESELLING <strong>EXCELLENCE</strong>
          </h3>
          <p
            class="leading-tight opacity-0 my-5 font-light"
            data-anim="fade"
            data-delay="0.2s"
          >
            We act as a strategic partner to provide access to essential,
            premium technology and build crucial alliances.
          </p>
        </div>
      </div>
    </div>

    <!-- Cards -->
    <div class="relative max-w-6xl mx-auto px-6 -mt-16 md:-mt-24">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <!-- Card 1 -->
        <div
          class="bg-[#7c3aed] text-white rounded-tr-[3rem] rounded-bl-[3rem] p-8 text-center flex flex-col justify-center min-h-[340px] md:w-full w-[280px] mx-auto"
        >
          <h4 class="text-2xl font-semibold mb-4">
            Resell premium software from industry leaders:
          </h4>
          <p class="text-lg md:text-2xl font-light leading-snug">
            Provide access to the best proven platforms.
          </p>
        </div>

        <!-- Card 2 -->
        <div
          class="bg-[#1e1b4b] text-white rounded-tr-[3rem] rounded-bl-[3rem] p-8 text-center flex flex-col justify-center min-h-[340px] md:w-full w-[280px] mx-auto"
        >
          <h4 class="text-2xl font-semibold mb-4">
            Build strategic alliances for unparalleled value:
          </h4>
          <p class="text-lg md:text-2xl font-light leading-snug">
            Expand capabilities through collaborations.
          </p>
        </div>

        <!-- Card 3 -->
        <div
          class="bg-[#7c3aed] text-white rounded-tr-[3rem] rounded-bl-[3rem] p-8 text-center flex flex-col justify-center min-h-[340px] md:w-full w-[280px] mx-auto"
        >
          <h4 class="text-2xl font-semibold mb-4">
            Provide access to cutting-edge tech:
          </h4>
          <p class="text-lg md:text-2xl font-light leading-snug">
            Ensure our clients are always equipped with future-ready tools.
          </p>
        </div>

        <!-- Card 4 -->
        <div
          class="bg-[#1e1b4b] text-white rounded-tr-[3rem] rounded-bl-[3rem] p-8 text-center flex flex-col justify-center min-h-[340px] md:w-full w-[280px] mx-auto"
        >
          <h4 class="text-2xl font-semibold mb-4">
            Drive client success across diverse markets:
          </h4>
          <p class="text-lg md:text-2xl font-light leading-snug">
            Match the right software solution to specific client needs globally.
          </p>
        </div>
      </div>
    </div>
  </section>

  <section class="relative overflow-hidden">
    <!-- Background image -->
    <img
      src="/images/ventures-bg.png"
      alt="Digiti background"
      class="absolute inset-0 w-full h-full object-cover"
    />

    <!-- Content -->
    <div
      class="relative max-w-4xl text-[#1E1B4E] mx-auto py-16 space-y-6 text-2xl md:text-[28px] text-center lg:px-0 px-6"
    >
      <div>
        <h3
          class="border border-[#1E1B4E] py-2 px-2 mb-4 md:text-3xl w-fit mx-auto"
        >
          LOCAL ADVANTAGE & STRATEGIC VENTURES
        </h3>
        <p
          class="leading-tight opacity-0 my-5 font-light"
          data-anim="fade"
          data-delay="0.2s"
        >
          Our
          <strong class="font-semibold">
            South African-based, Level 2 BBBEE-compliant team
          </strong>
          is dedicated to delivering high-quality, impactful solutions, ensuring
          local market compliance while adhering to global best practices.
        </p>

        <p
          class="leading-tight opacity-0 font-light"
          data-anim="fade"
          data-delay="0.6s"
        >
          Dijiti Solutions manages the South African team, providing the scope
          of work and overseeing project execution for flawless delivery.
        </p>

        <NuxtLink
          to="/contact"
          class="inline-flex items-center mt-8 justify-center px-10 py-4 rounded-full bg-white border border-white text-indigo-900 text-2xl md:text-3xl font-light tracking-wide transition-all duration-300 hover:bg-transparent hover:text-white"
        >
          Start Your Digital Transformation
        </NuxtLink>
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
