<template>
  <header>
    <Nav />
    <img src="@/assets/data/img/h3-rev-img-6.png" alt="pizza slice" />
    <PrevNextButton />
  </header>
</template>

<script>
import Nav from "@/components/Nav.vue";
import PrevNextButton from "@/components/PrevNextButton.vue";

export default {
  name: "headerComponent",
  components: {
    Nav,
    PrevNextButton,
  },
};
</script>

<style scoped lang="scss">
header {
  background-color: rgba($color: #000000, $alpha: 0.9);
  color: white;
  padding: 20px 0px;
  background-image: url(@/assets/data/img/h3-rev-img-5.png);
  background-repeat: no-repeat;
  background-position: center;
  position: relative;
}

img {
  margin: 25px 0px;
}
</style>