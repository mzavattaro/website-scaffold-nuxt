<template>
  <div
    class="flex flex-col items-center w-full px-6 mb-4 xl:px-0 sm:mx-auto text-primary max-w-7xl sm:mb-18"
  >
    <!-- TODO: Implement the pricing page here -->
    <div class="w-full mb-27">
      <Header />
    </div>

    <Hero />

    <PriceCard
      v-if="priceCards != null"
      v-for="priceCard in priceCards"
      :key="priceCard.id"
      :heading="priceCard.heading"
    />

    <div class="w-full mt-8 mb-10 sm:mb-18">
      <Card />
    </div>
    <div class="self-start w-full">
      <Footer />
    </div>
  </div>
</template>

<script lang="ts" setup>
const priceCards = ref([
  {
    id: 1,
    heading: "Basic Plan",
    description: "Our most popular plan.",
    price: "$5",
    duration: "Monthly",
    usps: [
      { item: "Create unlimited flashcards" },
      { item: "Export unlimited flashcards" },
      { item: "Migaku Cloud word syncing" },
      { item: "Track your known words" },
      { item: "Access to Pitch Trainer" },
    ],
  },
  {
    id: 2,
    heading: "Lifetime",
    description: "The most cost-effective plan.",
    price: "$199",
    duration: "Only once",
    usps: [
      { item: "Access to Alpha Builds" },
      { item: "Create unlimited flashcards" },
      { item: "Export unlimited flashcards" },
      { item: "Migaku Cloud word syncing" },
      { item: "Track your known words" },
      { item: "Access to Pitch Trainer" },
    ],
  },
  {
    id: 3,
    heading: "Try It",
    description: "Try before you buy.",
    price: "FREE",
    duration: "30 days",
    usps: [
      { item: "Create a Migaku account" },
      { item: "30-day free trial" },
      { item: "Create 100 flashcards" },
      { item: "Mass export 10 flashcards at a time" },
      { item: "No Migaku Cloud" },
    ],
  },
]);
</script>

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
