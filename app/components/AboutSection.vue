<template>
  <section class="relative overflow-hidden">
    <!-- Background image -->
    <img
      src="/images/about-gradient.png"
      alt="Digiti background"
      class="absolute inset-0 w-full h-full object-cover"
    />

    <!-- Content -->
    <div
      class="relative max-w-4xl text-white mx-auto py-16 space-y-6 text-2xl md:text-[28px] text-center lg:px-0 px-6"
    >
      <p class="leading-tight opacity-0" data-anim="fade" data-delay="0.2s">
        <strong class="font-semibold">
          With over 60 years of global experience, Dijiti Solutions designs,
          builds, and manages cutting-edge platforms that power modern finance,
          enterprise, and infrastructure.</strong
        >
      </p>

      <p
        class="leading-tight opacity-0 font-light"
        data-anim="fade"
        data-delay="0.6s"
      >
        From fintech and software development to construction technology and
        data analytics, Dijiti provides secure, intelligent, and scalable
        solutions that enable organisations to thrive in a rapidly evolving
        digital world.
      </p>

      <p
        class="leading-tight opacity-0 font-light"
        data-anim="fade"
        data-delay="1s"
      >
        Driven by innovation and built on a foundation of global expertise,
        Dijiti connects technology and opportunity, delivering results that
        empower businesses, strengthen economies, and enhance human progress.
      </p>
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
