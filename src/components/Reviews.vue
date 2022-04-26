<template>
  <section>
    <div class="container">
      <i class="fa-solid fa-quote-left"></i>
      <h3>
        "FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW
        YORK-STYLE PIZZA SLICE IN NAPLES"
      </h3>
      <h6>WASHINGTON POST 2018</h6>
      <div class="buttons">
        <button class="selected"></button>
        <button class="notSelected"></button>
        <button class="notSelected"></button>
      </div>
    </div>
    <PrevNextButton />
    <img src="@/assets/data/svg/svg-4.svg" alt="pizza slice" />
  </section>
</template>

<script>
import PrevNextButton from "@/components/PrevNextButton.vue";

export default {
  name: "reviewsItem",
  components: {
    PrevNextButton,
  },
};
</script>

<style scoped lang="scss">
section {
  background-image: url(@/assets/data/img/h3-testimonials-bckgrnd.jpg);
  background-repeat: no-repeat;
  background-position: center;
  display: flex;
  flex-direction: column;
  position: relative;

  .container {
    display: flex;
    flex-direction: column;
    row-gap: 10px;
    width: 40%;
    margin: 50px auto;

    i {
      font-size: 80px;
      color: #b7903c;
    }

    h3 {
      margin: 10px;
    }

    h6 {
      color: #b7903c;
    }

    .buttons {
      display: flex;
      justify-content: center;
      margin-top: 20px;
      column-gap: 5px;

      button {
        border-radius: 50%;
        width: 10px;
        height: 10px;
        border: none;
        margin-bottom: 10px;
      }
    }
  }

  .selected {
    background-color: #b7903c;
  }

  .notSelected {
    background-color: #e4e4d4;
  }

  img {
    width: 20px;
    align-self: flex-end;
    margin: 30px;
  }
}
</style>