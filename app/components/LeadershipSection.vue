<template>
  <section class="bg-white py-12 px-4 md:px-8 lg:px-16">
    <div class="max-w-7xl mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 lg:gap-12 items-center">
        <!-- Left Column: Text Content -->
        <div class="space-y-8">
          <!-- Section Title -->
          <div class="inline-block">
            <h2
              class="text-4xl md:text-5xl font-bold text-white bg-[#1a1b4e] px-6 py-3 mb-2 w-fit"
            >
              LEADERSHIP
            </h2>
            <h2
              class="text-4xl md:text-5xl font-bold text-white bg-[#1a1b4e] px-6 py-3 w-fit"
            >
              TEAM
            </h2>
          </div>

          <!-- Team Members Info -->
          <div class="space-y-8">
            <!-- Fred Coetzee -->
            <div>
              <h3 class="text-2xl md:text-3xl font-bold text-[#1a1b4e] mb-1">
                FRED COETZEE
              </h3>
              <p class="text-lg md:text-xl text-[#7c3aed] italic mb-3">
                Chief Executive Officer (Founding Member)
              </p>
              <p class="text-gray-700 text-base md:text-lg">
                25 years of IT experience, proven ability to lead large-scale,
                complex technology programmes with globally distributed teams.
              </p>
            </div>

            <!-- Blake Scriven -->
            <div>
              <h3 class="text-2xl md:text-3xl font-bold text-[#1a1b4e] mb-1">
                BLAKE SCRIVEN
              </h3>
              <p class="text-lg md:text-xl text-[#7c3aed] italic mb-3">
                Chief Operating Officer (Founding Member)
              </p>
              <p class="text-gray-700 text-base md:text-lg">
                15 years of legal and business expertise, skilled operational
                strategist leveraging AI and emerging technologies.
              </p>
            </div>
          </div>
        </div>

        <!-- Right Column: Photos -->
        <div class="flex flex-row gap-3">
          <!-- Fred Coetzee Photo -->
          <div class="relative">
            <img
              src="/images/Fred-Coetzee@300x-8.png?height=400&width=350"
              alt="Fred Coetzee"
              class="w-full h-auto"
            />
          </div>
          <!-- Blake Scriven Photo -->
          <div class="relative">
            <img
              src="/images/Blake-Scriven@300x-8.png?height=400&width=350"
              alt="Blake Scriven"
              class="w-full h-auto"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// No additional logic needed for this static component
</script>

<style scoped>
/* Additional styles if needed */
</style>
