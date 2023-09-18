<template>
  <div class="w-screen h-screen bg-gradient-to-br from-red-400 to-sky-200">
    <div class="flex justify-center items-center pt-4">
      <Avatar />
    </div>
    <div class="text-center text-white text-lg font-medium mt-2 pb-4">
      <h1>Coding Station</h1>
      <h2>Michelle</h2>
    </div>
    <div>
      <CardLinks v-for="(link, idx) in links" :key="idx" :link="link" />
    </div>
  </div>
</template>

<script setup>
const links = [
  {
    link: "https://github.com/michellejt",
    text: "Github",
    icon: "github",
  },
];
</script>
