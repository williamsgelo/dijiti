<template>
  <section class="relative w-full">
    <!-- Desktop: Image as background with text overlay -->
    <div class="hidden md:block relative w-full h-[550px]">
      <!-- Background Image -->
      <div class="absolute inset-0">
        <NuxtImg
          src="/images/Desktop-Contact.png"
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
            QUESTIONS?
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              OUR SPECIALISTS ARE
            </span>
            <span
              class="block bg-[#1E1B4E] text-white px-6 py-2 mt-2 inline-block"
            >
              READY TO HELP
            </span>
          </h1>

          <p class="text-2xl text-gray-600 mb-8 leading-relaxed max-w-sm">
            Let's discuss how our execution expertise can drive your business
            forward.
          </p>
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
          QUESTIONS?
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block uppercase"
          >
            OUR SPECIALISTS ARE
          </span>
          <span
            class="block bg-[#1E1B4E] text-white px-4 py-2 mt-2 inline-block uppercase"
          >
            READY TO HELP
          </span>
        </h1>

        <p class="text-lg text-gray-600 mb-6 leading-relaxed">
          Let's discuss how our execution expertise can drive your business
          forward.
        </p>
      </div>

      <!-- Image Below -->
      <div class="w-full hidden">
        <NuxtImg
          src="/images/Mobile-Contact.png"
          alt="Business professionals collaborating"
          class="w-full h-auto object-cover"
        />
      </div>
    </div>
  </section>
  <section>
    <div class="bg-gray-200 flex items-center justify-center py-14 px-4">
      <form @submit.prevent="handleSubmit" class="w-full max-w-6xl">
        <div class="grid md:grid-cols-2 gap-4">
          <!-- Left Column - Input Fields -->
          <div class="flex flex-col gap-4">
            <input
              v-model="form.fullName"
              type="text"
              placeholder="Full Name"
              class="w-full px-6 py-5 bg-white text-gray-400 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-indigo-900 transition-all"
              required
            />
            <input
              v-model="form.email"
              type="email"
              placeholder="Email"
              class="w-full px-6 py-5 bg-white text-gray-400 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-indigo-900 transition-all"
              required
            />
            <input
              v-model="form.phone"
              type="tel"
              placeholder="Phone Number"
              class="w-full px-6 py-5 bg-white text-gray-400 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-indigo-900 transition-all"
            />
            <input
              v-model="form.company"
              type="text"
              placeholder="Company"
              class="w-full px-6 py-5 bg-white text-gray-400 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-indigo-900 transition-all"
            />
          </div>

          <!-- Right Column - Message Textarea and Button -->
          <div class="flex flex-col gap-4">
            <textarea
              v-model="form.message"
              placeholder="Your Message"
              rows="8"
              class="w-full h-full min-h-[200px] px-6 py-5 bg-white text-gray-400 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-indigo-900 resize-none transition-all"
              required
            ></textarea>
            <button
              type="submit"
              class="md:ml-auto px-8 py-4 bg-indigo-950 text-white font-medium tracking-wider rounded-md hover:bg-indigo-900 transition-colors"
            >
              SEND MESSAGE >
            </button>
          </div>
        </div>
      </form>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from "vue";

const form = ref({
  fullName: "",
  email: "",
  phone: "",
  company: "",
  message: "",
});

const handleSubmit = () => {
  console.log("Form submitted:", form.value);
  // Add your form submission logic here
  alert("Message sent successfully!");

  // Reset form
  form.value = {
    fullName: "",
    email: "",
    phone: "",
    company: "",
    message: "",
  };
};

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
