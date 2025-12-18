<template>
  <nav class="w-full bg-white b z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-20">
        <!-- Logo -->
        <div class="h-44 w-24 md:h-28 md:w-28">
          <NuxtLink to="/" class="text-4xl font-bold uppercase">
            <img
              src="/images/dijiti-logo.svg"
              alt="Digiti Logo"
              class="h-full w-full object-contain"
            />
          </NuxtLink>
        </div>

        <!-- Desktop Navigation -->
        <div class="hidden md:block animate-fade-in">
          <div class="ml-10 flex items-baseline space-x-8 uppercase">
            <NuxtLink
              to="/about"
              class="block text-[#1E1B4E] hover:text-primary-600 px-3 py-2 tracking-[0.3em] border-b-[5px] border-transparent pb-1"
              active-class="!border-[#1E1B4E]"
            >
              About Us
            </NuxtLink>
            <NuxtLink
              to="/services"
              class="block text-[#1E1B4E] hover:text-primary-600 px-3 py-2 tracking-[0.3em] border-b-[5px] border-transparent pb-1"
              active-class="!border-[#1E1B4E]"
            >
              Services
            </NuxtLink>
            <NuxtLink
              to="/our-work"
              class="block text-[#1E1B4E] hover:text-primary-600 px-3 py-2 tracking-[0.3em] border-b-[5px] border-transparent pb-1"
              active-class="!border-[#1E1B4E]"
            >
              Our Work
            </NuxtLink>
            <NuxtLink
              to="/resources"
              class="block text-[#4B0082] hover:text-primary-600 px-3 py-2 tracking-[0.3em] border-b-[5px] border-transparent pb-1"
              active-class="!border-[#1E1B4E]"
            >
              Resources
            </NuxtLink>
            <NuxtLink
              to="/contact"
              class="block text-[#1E1B4E] hover:text-primary-600 px-3 py-2 tracking-[0.3em] border-b-[5px] border-transparent pb-1"
              active-class="!border-[#1E1B4E]"
            >
              Contact Us
            </NuxtLink>
          </div>
        </div>

        <!-- Mobile menu button -->
        <div class="md:hidden">
          <button
            @click="mobileMenuOpen = !mobileMenuOpen"
            class="inline-flex items-center justify-center p-2 rounded-md text-[#1E1B4E]"
          >
            <svg
              class="h-8 w-8"
              :class="{ hidden: mobileMenuOpen, block: !mobileMenuOpen }"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
            <svg
              class="h-6 w-6"
              :class="{ block: mobileMenuOpen, hidden: !mobileMenuOpen }"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile menu -->
    <div
      class="md:hidden transition-all duration-300 ease-in-out"
      :class="{
        'max-h-64 opacity-100': mobileMenuOpen,
        'max-h-0 opacity-0 overflow-hidden': !mobileMenuOpen,
      }"
    >
      <div class="px-2 pt-2 pb-3 space-y-1 bg-white border-t border-gray-200">
        <NuxtLink
          to="/about"
          class="block px-3 py-2 text-base font-medium text-[#1E1B4E] rounded-md transition-colors uppercase"
        >
          About Us
        </NuxtLink>
        <NuxtLink
          to="/services"
          class="block px-3 py-2 text-base font-medium text-[#1E1B4E] rounded-md transition-colors uppercase"
        >
          Services
        </NuxtLink>
        <NuxtLink
          to="/"
          class="block px-3 py-2 text-base font-medium text-[#1E1B4E] rounded-md transition-colors uppercase"
        >
          Our Work
        </NuxtLink>
        <NuxtLink
          to="/resources"
          class="block px-3 py-2 text-base font-medium text-[#1E1B4E] rounded-md transition-colors uppercase"
        >
          Resources
        </NuxtLink>
        <div class="pb-3 bg-white border-gray-200">
          <NuxtLink
            to="/contact"
            class="block px-3 py-2 text-base font-medium text-[#1E1B4E] rounded-md transition-colors uppercase"
          >
            Contact Us
          </NuxtLink>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
const mobileMenuOpen = ref(false);

// Close mobile menu when clicking outside or on route change
const route = useRoute();
watch(
  () => route.path,
  () => {
    mobileMenuOpen.value = false;
  }
);
</script>
