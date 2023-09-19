<template>
  <div :class="modelValue ? 'visible' : 'invisible'">
    <div
      class="bg-black opacity-30 fixed top-0 left-0 w-full h-full transition-all duration-300 ease-in-out"
      :class="!modelValue ? 'opacity-0' : 'opacity-50'"
    ></div>

    <div
      class="fixed left-0 top-0 z-30 h-full w-full flex items-center transition-all duration-300 ease-in-out"
      :class="`${
        !modelValue
          ? 'opacity-0 translate-y-[-50px]'
          : 'opacity-100 translate-y-[0px]'
      }`"
    >
      <div class="bg-white z-50 w-auto m-auto p-4 rounded-lg">
        <div class="flex items-center justify-between mb-10">
          <p class="text-gray-800 font-medium text-lg">Share this page</p>
          <button
            @click="close()"
            type="button"
            class="bg-gray-300 w-7 h-7 flex justify-center items-center rounded-full"
          >
            <Icon name="mdi:close" size="20" />
          </button>
        </div>
        <div class="flex itmes-center justify-between">
          <div class="flex items-center">
            <Icon name="mdi:whatsapp" color="green" size="20" />
            <a
              href="https://wa.me/?text=https://link-share-mjt.netlify.app"
              target="_blank"
            >
              <span class="ml-2 text-gray-800 text-lg mr-8"
                >Share with whatsapp</span
              >
            </a>
          </div>
          <Icon name="mdi:chevron-right" color="gray" size="30" />
        </div>
        <div
          @click="shareLink()"
          class="cursor-pointer flex justify-between border-2 border-gray-200 p-2 mt-8 rounded items-center"
        >
          <Icon name="mdi:content-copy" />
          <p class="mx-4">link-share-mjt.netlify.app</p>
          <p
            class="font-medium"
            :class="`${copy === 'Copy' ? 'text-gray-800' : 'text-green-800'}`"
          >
            {{ copy }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps(["modelValue"]);
const emits = defineEmits("update:modelValue");
let copy = ref("Copy");

function shareLink() {
  navigator.clipboard.writeText("https://link-share-mjt.netlify.app");
  copy.value = "Copied";
}

function close() {
  emits("update:modelValue", false);
  copy.value = "Copy";
}
</script>
