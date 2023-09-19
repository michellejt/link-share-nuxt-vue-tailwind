<template>
  <div
    class="bg-white flex items-center rounded-full p-4 w-full mx-4 max-w-md shadow-lg shadow-red-500 cursor-pointer"
    @click="goTo(link.link)"
  >
    <Icon :name="`mdi:${link.icon}`" class="-mr-8" size="32" color="tomato" />

    <p class="font-bold px-2 m-auto">{{ link.text }}</p>
  </div>
</template>

<script setup>
defineProps({
  link: {
    type: Object,
  },
});

function goTo(link) {
  window.open(link, "_blank");
}
</script>
