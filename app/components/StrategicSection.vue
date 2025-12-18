<template>
  <section class="relative overflow-hidden">
    <!-- Background image -->
    <img
      src="/images/ventures-bg.png"
      alt="Digiti background"
      class="absolute inset-0 w-full h-full object-cover"
    />

    <!-- Content -->
    <div
      class="relative max-w-4xl text-[#1E1B4E] mx-auto py-16 space-y-6 text-2xl text-center lg:px-0 px-6"
    >
      <div>
        <h3 class="border border-[#1E1B4E] py-2 px-2 mb-4 w-fit mx-auto">
          LOCAL ADVANTAGE & STRATEGIC VENTURES
        </h3>
        <p
          class="leading-tight opacity-0 my-5 font-light"
          data-anim="fade"
          data-delay="0.2s"
        >
          As a proudly South African company, our
          <strong class="font-semibold"> Level 2 BBBEE-compliant </strong> team
          ensures high-quality, impactful delivery.
        </p>

        <p
          class="leading-tight opacity-0 font-light"
          data-anim="fade"
          data-delay="0.6s"
        >
          Our 40% ownership in Word of Mouth (smart lead generation) expands our
          reach,
          <strong class="font-semibold"> boosts economic growth, </strong> and
          creates business opportunities for everyday South Africans.
        </p>
      </div>

      <div class="flex justify-center">
        <NuxtImg
          src="/images/wom-logo.png"
          alt="Word of Mouth Logo"
          class="w-80 h-48 object-contain"
        />
      </div>
    </div>
  </section>
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
