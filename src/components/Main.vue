<template>
  <main>
    <Place />
    <Reviews />
  </main>
</template>

<script>
import Place from "@/components/Place.vue";
import Reviews from "@/components/Reviews.vue";

export default {
  name: "MainComponent",
  components: {
    Place,
    Reviews,
  },
};
</script>

<style>
</style>