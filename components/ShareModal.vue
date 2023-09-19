<template>
  <div>
    <div class="bg-black opacity-30 fixed top-0 left-0 w-full h-full"></div>

    <div class="fixed left-0 top-0 z-30 h-full w-full flex items-center">
      <div class="bg-white z-50 w-auto m-auto p-4 rounded-lg">
        <div class="flex items-center justify-between mb-10">
          <p>Share this page</p>
          <button>
            <Icon name="mdi:close" size="20" />
          </button>
        </div>
        <div class="flex itmes-center justify-between">
          <div class="flex items-center">
            <Icon name="mdi:whatsapp" color="green" size="20" />
            <a href="https://wa.mt?text=https://michellejt.com" target="_blank">
              <span class="ml-2 text-gray-800 text-lg mr-8"
                >Share with whatsapp</span
              >
            </a>
          </div>
          <Icon name="mdi:chevron-right" color="gray" size="30" />
        </div>
        <div
          class="flex justify-between border-2 border-gray-200 p-2 mt-8 rounded items-center"
        >
          <Icon name="mdi:content-copy" />
          <p class="mx-4">michelle.jst.com</p>
          <p class="font-medium">{{ copy }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
let copy = ref("Copy");
</script>
