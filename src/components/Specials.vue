<template>
  <section>
    <div class="poster">
      <img src="@/assets/data/img/h1-img-7n.png" alt="Special" />
    </div>
    <div class="specials">
      <div class="container">
        <h1>SPECIALS*</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Hic cumque
          ut dicta animi perspiciatis at similique impedit necessitatibus
          aperiam!
        </p>

        <div class="combos" v-for="(food, index) in menu" :key="index">
          <div class="price">
            <h3>{{ food.price }}</h3>
          </div>
          <div class="text">
            <h3>{{ food.name }}</h3>
            <p>
              {{ food.description }}
            </p>
          </div>
        </div>
      </div>

      <div class="slice">
        <a href="#">
          <img src="@/assets/data/svg/svg-4.svg" alt="pizza slice" />
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "sectionItem",
  data() {
    return {
      menu: [
        {
          price: "$10",
          name: "COMBO PICCOLO",
          description: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Hic
              cumque ut dicta animi perspiciatis at similique impedit
              necessitatibus aperiam!`,
        },
        {
          price: "$20",
          name: "COMBO MEZZO",
          description: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Hic
              cumque ut dicta animi perspiciatis at similique impedit
              necessitatibus aperiam!`,
        },
        {
          price: "$30",
          name: "COMBO GRANDE",
          description: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Hic
              cumque ut dicta animi perspiciatis at similique impedit
              necessitatibus aperiam!`,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
section {
  display: flex;
  margin: 10px 0px;

  .poster {
    width: calc(100% / 2);
    background-image: url(@/assets/data/img/h1-img-4.jpg);
    background-size: cover;
    padding: 50px 0px;

    img {
      margin: 100px 0px;
    }
  }

  .specials {
    width: calc(100% / 2);
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: left;
    position: relative;

    h1 {
      font-size: 30px;
    }

    .container {
      width: 50%;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      row-gap: 20px;

      .combos {
        display: flex;
        column-gap: 20px;

        .price {
          color: #ac432a;
        }

        .text {
          display: flex;
          flex-direction: column;
          row-gap: 10px;
        }
      }

      p {
        color: grey;
      }
    }

    img {
      width: 20px;
      align-self: flex-end;
      margin: 30px;
    }
  }
}
.slice {
  background-color: #f6f7f2;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  position: absolute;
  right: 20px;
  top: 70%;
  img {
    width: 20px;
  }
}
</style>