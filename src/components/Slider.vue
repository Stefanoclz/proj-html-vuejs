<template>
  <div class="container-slide" @mouseup="changePress">
    <div
      class="slider"
      @mousedown="keepEvent($event)"
      @mouseenter="changeCursor"
      @mouseup="changeCursor"
      @mousemove="moveSlider($event)"
    >
      <div class="slider-inner" @click="keepOffset($event)">
        <div class="card" v-for="(pizza, index) in mainPizze" :key="index">
          <img
            :src="require(`@/assets/data/img/h3-product-img-${pizza.link}.png`)"
            alt="pizza Bismarck"
          />
          <div class="sold" v-if="pizza.sold === true">
            <h6>SOLD</h6>
          </div>
          <h4 class="nomePizza">{{ pizza.name }}</h4>
          <h4 class="prezzo">{{ pizza.price }}</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SliderItem",
  data() {
    return {
      mainPizze: [
        {
          link: "1a-100x100",
          name: "BISMARCK",
          price: "$15.00 - $30.00",
          sold: false,
        },
        {
          link: "2a-150x150",
          name: "FIORI DI ZUCCA",
          price: "$7.00 - $50.00",
          sold: false,
        },
        {
          link: "3a-150x150",
          name: "VALDOSTANA",
          price: "$55.00",
          sold: true,
        },
        {
          link: "4a-150x150",
          name: "PIZZA TARTUFATA",
          price: "$45.00",
          sold: false,
        },
        {
          link: "5a-150x150",
          name: "FRANCESCANA",
          price: "$25.00",
          sold: false,
        },
        {
          link: "6a-100x100",
          name: "CAMPAGNOLA",
          price: "$50.00 - $95.00",
          sold: false,
        },
      ],
      Pressed: false,
      startX: "",
      x: "",
    };
  },
  methods: {
    keepEvent(e) {
      let slider = document.querySelector(".slider");
      let innerSlider = document.querySelector(".slider-inner");
      this.Pressed = true;
      this.startX = e.offsetX - innerSlider.offsetLeft;
      console.log(innerSlider.offsetLeft);
      slider.style.cursor = "grabbing";
    },
    changeCursor() {
      let slider = document.querySelector(".slider");
      slider.style.cursor = "grab";
    },
    moveSlider(e) {
      let innerSlider = document.querySelector(".slider-inner");
      if (!this.Pressed) return;
      e.preventDefault();

      this.x = e.offsetX;
      innerSlider.style.left = `${this.x - this.startX}px`;

      this.checkLimit();
    },
    changePress() {
      this.Pressed = false;
    },
    checkLimit() {
      /*let slider = document.querySelector(".slider");*/
      let innerSlider = document.querySelector(".slider-inner");
      /*let outer = slider.getBoundingClientRect();
      let inner = innerSlider.getBoundingClientRect();*/

      if (parseInt(innerSlider.style.left) > 0) {
        innerSlider.style.left = "0px";
      } else if (parseInt(innerSlider.style.left) < -420) {
        innerSlider.style.left = "-410px";
      }
    },
  },
};
</script>

<style scoped lang="scss">
.container-slide {
  position: relative;
  width: 100%;
  height: 100%;
  margin: 30px 0px;
}

.slider {
  position: relative;
  width: 100%;
  height: 300px;
  overflow: hidden;
  margin-bottom: 100px;
}

.slider-inner {
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  column-gap: 150px;
  height: 100%;
  width: 200%;
  pointer-events: none;
  transition: 0s ease-in;
  padding: 0px 20px;
}

.card {
  display: flex;
  flex-direction: column;
  row-gap: 10px;
  justify-content: center;
  text-align: center;
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
}

.nomePizza {
  color: #c5a662;
}

.prezzo {
  color: #d24220;
}
</style>