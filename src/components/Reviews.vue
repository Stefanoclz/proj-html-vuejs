<template>
  <section>
    <div class="container">
      <i class="fa-solid fa-quote-left"></i>
      <div
        v-for="(review, index) in reviews"
        :key="index"
        v-show="reviewId === index"
      >
        <h3>{{ review.review }}</h3>
        <h6>{{ review.author }}</h6>
      </div>
      <div class="buttons">
        <button class="selected"></button>
        <button class="notSelected"></button>
        <button class="notSelected"></button>
      </div>
    </div>
    <PrevNextButton @goBack="PrevReview" @goForward="NextReview" />
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
  data() {
    return {
      reviewId: 0,
      reviews: [
        {
          review: `"FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW
        YORK-STYLE PIZZA SLICE IN NAPLES"`,
          author: "WASHINGTON POST 2018",
          id: 1,
        },
        {
          review: `"THE CRUST IS SO TENDER IT BARELY FIGHTS FORK, KNIFE OR TEETH."`,
          author: "NEW YORK TIMES 2019",
          id: 2,
        },
        {
          review: `"PROBABLY THE BEST RESTAURANT IN THE AREA, VERY GOOD AND VERY LIGHT PIZZA, PERFECT WELCOME"`,
          author: "DAILY POST 2020",
          id: 3,
        },
      ],
    };
  },
  methods: {
    PrevReview() {
      this.reviewId--;
      if (this.reviewId < 0) {
        this.reviewId = 2;
        console.log("review", this.reviewId);
      }
    },
    NextReview() {
      this.reviewId++;
      if (this.reviewId > 2) {
        this.reviewId = 0;
        console.log("review", this.reviewId);
      }
    },
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