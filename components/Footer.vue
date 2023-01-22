<template>
  <div
    class="grid w-full grid-cols-2 gap-4 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-6"
  >
    <div
      class="font-bold"
      v-if="items != null"
      v-for="item in items"
      :key="item.id"
    >
      {{ item.heading }}
      <div
        class="text-primary/[.6] py-1 font-medium"
        v-for="link in item.links"
      >
        <a href="/">
          {{ link.link }}
        </a>
      </div>
    </div>
  </div>

  <div
    class="flex flex-col items-center justify-center mt-10 sm:justify-between sm:flex-row"
  >
    <div class="mb-6 sm:mb-0">
      <UiSvg name="migaku-logo-mono" />
    </div>
    <div class="flex mb-6 sm:mb-0">
      <UiSvg class="pr-11" name="facebook-mono" />
      <UiSvg class="pr-11" name="twitter-mono" />
      <UiSvg class="pr-11" name="instagram-mono" />
      <UiSvg name="discord-mono" />
    </div>
    <span class="text-primary/[.6]">©2022 Migaku</span>
  </div>
</template>

<!-- Component to render an SVG found in `@/assets/svg/<name>.svg` -->
<script lang="ts" setup>
const items = ref([
  {
    id: 1,
    heading: "Products",
    links: [
      { link: "Browser extension" },
      { link: "Anki add-on" },
      { link: "Kanji God add-on" },
    ],
  },
  {
    id: 2,
    heading: "Use cases",
    links: [
      { link: "Input-based learning" },
      { link: "Immersive learning" },
      { link: "Popup dictionary" },
      { link: "Video flashcards" },
    ],
  },
  {
    id: 3,
    heading: "Help!",
    links: [
      { link: "Support" },
      { link: "Join the Discord" },
      { link: "Video guides" },
    ],
  },
  {
    id: 4,
    heading: "Brand",
    links: [{ link: "Partnerships" }, { link: "Press Kit" }],
  },
  {
    id: 5,
    heading: "Resources",
    links: [
      { link: "Support us on Patreon" },
      { link: "Youtube" },
      { link: "Reddit" },
      { link: "Privacy policy" },
      { link: "Terms" },
    ],
  },
  {
    id: 6,
    heading: "Company",
    links: [
      { link: "About" },
      { link: "Roadmap" },
      { link: "Partners" },
      { link: "Jobs" },
      { link: "Blog" },
    ],
  },
]);
</script>
