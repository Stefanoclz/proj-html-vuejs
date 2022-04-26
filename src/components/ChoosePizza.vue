<template>
  <section>
    <div class="container">
      <h6>CHOOSE YOUR FLAVOUR</h6>
      <h1>THE BEST PIZZA MENU IN TOWN</h1>
      <P
        >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fuga, sequi
        labore praesentium nulla</P
      >
    </div>
    <div class="slice">
      <a href="#">
        <img src="@/assets/data/svg/svg-4.svg" alt="pizza slice" />
      </a>
    </div>
    <PizzaSlider />
  </section>
</template>

<script>
import PizzaSlider from "@/components/PizzaSlider.vue";

export default {
  name: "choosePizza",
  components: {
    PizzaSlider,
  },
};
</script>

<style scoped lang="scss">
section {
  position: relative;
}

.container {
  width: 30%;
  margin: 100px auto;
  display: flex;
  flex-direction: column;
  row-gap: 10px;
}

.slice {
  background-color: white;
  width: 40px;
  padding: 7px 0px;
  border-radius: 50%;
  text-align: center;
  position: absolute;
  right: 20px;
  top: 20%;
  img {
    width: 20px;
  }
}
</style>