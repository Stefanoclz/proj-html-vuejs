<template>
  <div class="containerPizze" @mousedown="dragList($event)">
    <div class="card">
      <img
        src="@/assets/data/img/h3-product-img-1a-100x100.png"
        alt="pizza Bismarck"
      />
      <h4 class="nomePizza">BISMARCK</h4>
      <h4 class="prezzo"><span>$15.00</span> $30.00</h4>
    </div>

    <div class="card">
      <img
        src="@/assets/data/img/h3-product-img-2a-150x150.png"
        alt="pizza Bismarck"
      />
      <h4 class="nomePizza">FIORI DI ZUCCA</h4>
      <h4 class="prezzo">$7.00 - $50.00</h4>
    </div>

    <div class="card">
      <img
        src="@/assets/data/img/h3-product-img-3a-150x150.png"
        alt="pizza Bismarck"
      />
      <div class="sold">
        <h6>SOLD</h6>
      </div>
      <h4 class="nomePizza">VALDOSTANA</h4>
      <h4 class="prezzo">$55.00</h4>
    </div>

    <div class="card">
      <img
        src="@/assets/data/img/h3-product-img-4a-150x150.png"
        alt="pizza Bismarck"
      />
      <h4 class="nomePizza">PIZZA TARTUFATA</h4>
      <h4 class="prezzo">$45.00</h4>
    </div>

    <div class="card">
      <img
        src="@/assets/data/img/h3-product-img-5a-150x150.png"
        alt="pizza Bismarck"
      />
      <h4 class="nomePizza">FRANCESCANA</h4>
      <h4 class="prezzo">$25.00</h4>
    </div>

    <div class="card">
      <img
        src="@/assets/data/img/h3-product-img-6a-100x100.png"
        alt="pizza Bismarck"
      />
      <h4 class="nomePizza">CAMPAGNOLA</h4>
      <h4 class="prezzo">$50.00 - $95.00</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "pizzaSlider",
  data() {
    return {
      evento: "",
    };
  },
  methods: {
    dragList($event) {
      console.log("test", $event.offsetX);
    },
  },
};
</script>

<style scoped lang="scss">
.containerPizze {
  display: flex;
  flex-wrap: nowrap;
  margin-bottom: 150px;
  column-gap: 120px;
  justify-content: center;
  overflow-x: hidden;

  .card {
    display: flex;
    flex-direction: column;
    row-gap: 10px;
    position: relative;

    .sold {
      position: absolute;
      top: 5%;
      right: 5%;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      background-color: #d2401e;
      color: white;
      line-height: 60px;
    }

    img {
      width: 250px;
    }

    .nomePizza {
      color: #c5a662;
    }

    .prezzo {
      color: #d24220;

      span {
        color: #d3cfaf;
      }
    }
  }
}
</style>