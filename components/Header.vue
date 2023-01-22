<template>
  <div class="items-center hidden w-full sm:flex sm:justify-between mt-7">
    <div class="flex">
      <div
        class="flex mr-6 text-lg font-bold"
        v-if="items != null"
        v-for="item in items"
      >
        <a href="/">{{ item.link }}</a>
      </div>
    </div>
    <div class="-ml-6">
      <UiSvg name="migaku-logo-color" />
    </div>
    <div class="flex items-center">
      <div class="mr-6 text-lg font-bold">Log in</div>
      <button
        class="px-4 rounded-full py-2.5 bg-gradient-to-b from-morning-sun to-rose"
      >
        <p class="font-bold text-white">Get started</p>
      </button>
    </div>
  </div>
</template>

<!-- Component to render an SVG found in `@/assets/svg/<name>.svg` -->
<script lang="ts" setup>
const items = ref([
  {
    id: 1,
    link: "Starter Guide",
  },
  {
    id: 2,
    link: "Help",
  },
  {
    id: 3,
    link: "Blog",
  },
  {
    id: 4,
    link: "Pricing",
  },
]);
</script>
