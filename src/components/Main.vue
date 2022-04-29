<template>
  <main>
    <Place />
    <Reviews />
    <Specials />
    <PizzaBuild />
    <People />
    <div class="sponsor">
      <div class="container">
        <div class="brand" v-for="(logo, index) in brandsLogos" :key="index">
          <img
            :src="require(`@/assets/data/img/h1-clients-img-${logo.id}.png`)"
            :alt="logo.alt"
          />
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
  data() {
    return {
      brandsLogos: [
        {
          id: "4",
          alt: "Cowboy",
        },
        {
          id: "3",
          alt: "Gordon",
        },
        {
          id: "1",
          alt: "Big Cheese",
        },
        {
          id: "2",
          alt: "Bludoos Bar",
        },
        {
          id: "5",
          alt: "Vegan",
        },
      ],
    };
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