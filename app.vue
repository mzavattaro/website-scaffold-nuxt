<template>
  <div
    class="flex flex-col items-center w-full px-6 xl:px-0 sm:mx-auto text-primary max-w-7xl"
  >
    <!-- TODO: Implement the pricing page here -->
    <!-- <Header /> -->
    <div class="w-full mb-10 sm:mb-18">
      <Card />
    </div>
    <div class="self-start w-full">
      <Footer />
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style lang="scss">
// CSS reset
@import url("@/assets/styles/preflight.css");

// Fonts & typography
@import url("@/assets/fonts/GT-Maru/gt-maru.css");
@import url("@/assets/fonts/Inter/inter.css");
@import url("@/assets/styles/typography.css");

// Theme
@import url("@/assets/styles/colors.css");

// Mixins
@import url("@/assets/styles/mixins.scss");
</style>
