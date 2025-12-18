<template>
  <a
    class="scroll-to-top scroll-to-target"
    :class="{ 'd-block': scroll }"
    aria-label="Click to go back to top of page"
    href="#"
    ><span class="hover:scale-150"
      ><img
        src="/images/Back-to-Top.svg"
        width="40"
        height="40"
        alt="Back to Top Button" /></span
  ></a>
</template>

<script setup>
import { onMounted, onUnmounted, ref } from "vue";
const scroll = ref(false);

const handleScroll = () => {
  const scrollCheck = window.scrollY > 100;
  if (scrollCheck !== scroll.value) {
    scroll.value = scrollCheck;
  }
};

onMounted(() => {
  document.addEventListener("scroll", handleScroll);
});
onUnmounted(() => {
  document.removeEventListener("scroll", handleScroll);
});
</script>

<style scoped>
span {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
