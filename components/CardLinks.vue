<template>
  <div class="">
    <Icon :name="`mdi:${link.icon}`" />

    <p>{{ link.text }}</p>
  </div>
</template>

<script setup>
defineProps({
  link: {
    type: Object,
  },
});
</script>
