<template>
  <span v-if="icon" v-html="icon" />
</template>

<!-- Component to render an SVG found in `@/assets/svg/<name>.svg` -->
<script lang="ts" setup>
const props = defineProps<{
  name?: string;
}>();

// Use Vite's glob import to get all SVGs from assets
const icons = Object.fromEntries(
  Object.entries(import.meta.glob("~/assets/svg/*.svg", { as: "raw" })).map(
    ([key, value]) => {
      const filename = key.split("/").pop()!.split(".").shift();
      return [filename, value];
    }
  )
);

// Lazily load the correct icon
const icon = props.name && (await icons?.[props.name]?.());
</script>
