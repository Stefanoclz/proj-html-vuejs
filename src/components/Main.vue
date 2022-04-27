<template>
  <main>
    <Place />
    <Reviews />
    <Specials />
    <PizzaBuild />
    <People />
    <div class="sponsor">
      <div class="container">
        <div class="brand">
          <img src="@/assets/data/img/h1-clients-img-4.png" alt="Cowboy" />
        </div>
        <div class="brand">
          <img src="@/assets/data/img/h1-clients-img-3.png" alt="Gordon" />
        </div>
        <div class="brand">
          <img src="@/assets/data/img/h1-clients-img-1.png" alt="Big Cheese" />
        </div>
        <div class="brand">
          <img src="@/assets/data/img/h1-clients-img-2.png" alt="Bludoos Bar" />
        </div>
        <div class="brand">
          <img src="@/assets/data/img/h1-clients-img-5.png" alt="Vegan" />
        </div>
      </div>
    </div>
    <ChoosePizza />
    <Events />
  </main>
</template>

<script>
import Place from "@/components/Place.vue";
import Reviews from "@/components/Reviews.vue";
import Specials from "@/components/Specials.vue";
import PizzaBuild from "@/components/PizzaBuild.vue";
import People from "@/components/People.vue";
import ChoosePizza from "@/components/ChoosePizza.vue";
import Events from "@/components/Events.vue";

export default {
  name: "MainComponent",
  components: {
    Place,
    Reviews,
    Specials,
    PizzaBuild,
    People,
    ChoosePizza,
    Events,
  },
};
</script>

<style scoped lang="scss">
.sponsor {
  background-color: #f7f7f2;
  margin-bottom: 10px;
  .container {
    width: 60%;
    margin: 0 auto;
    display: flex;
    column-gap: 2%;
    padding: 50px 0px;

    .brand {
      width: calc(100% / 5) - 2%;
    }
  }
}
</style>