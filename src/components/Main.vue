<template>
  <main>
    <Place />
    <Reviews />
    <Specials />
    <PizzaBuild />
    <People />
  </main>
</template>

<script>
import Place from "@/components/Place.vue";
import Reviews from "@/components/Reviews.vue";
import Specials from "@/components/Specials.vue";
import PizzaBuild from "@/components/PizzaBuild.vue";
import People from "@/components/People.vue";

export default {
  name: "MainComponent",
  components: {
    Place,
    Reviews,
    Specials,
    PizzaBuild,
    People,
  },
};
</script>

<style>
</style>