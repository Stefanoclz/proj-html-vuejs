<template>
  <main>
    <Place />
    <Reviews />
    <Specials />
    <PizzaBuild />
  </main>
</template>

<script>
import Place from "@/components/Place.vue";
import Reviews from "@/components/Reviews.vue";
import Specials from "@/components/Specials.vue";
import PizzaBuild from "@/components/PizzaBuild.vue";

export default {
  name: "MainComponent",
  components: {
    Place,
    Reviews,
    Specials,
    PizzaBuild,
  },
};
</script>

<style>
</style>