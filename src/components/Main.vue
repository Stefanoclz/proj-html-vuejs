<template>
  <main>
    <Place />
    <Reviews />
    <Specials />
  </main>
</template>

<script>
import Place from "@/components/Place.vue";
import Reviews from "@/components/Reviews.vue";
import Specials from "@/components/Specials.vue";

export default {
  name: "MainComponent",
  components: {
    Place,
    Reviews,
    Specials,
  },
};
</script>

<style>
</style>