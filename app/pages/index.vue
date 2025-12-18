<template>
  <div>
    <Hero />
    <AboutSection />
    <StrategicSection />
    <PartnersSection />

    <div class="floating-button">
      <LazyBackToTop />
    </div>
  </div>
</template>

<script setup lang="ts">
useSeoMeta({
  title: "Dijiti Solutions | Global Software Expertise & Technology Consulting",
  ogTitle:
    "Dijiti Solutions | Global Software Expertise & Technology Consulting",
  description:
    "TDijiti Solutions delivers cutting-edge software expertise and world-class technology consulting. We solve complex problems and drive client success globally.",
  ogDescription:
    "Dijiti Solutions delivers cutting-edge software expertise and world-class technology consulting. We solve complex problems and drive client success globally.",
  ogImage: "https://example.com/image.png",
  twitterCard: "summary_large_image",
});
</script>
