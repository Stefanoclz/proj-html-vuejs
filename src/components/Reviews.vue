<template>
  <section>
    <div class="container">
      <i class="fa-solid fa-quote-left"></i>
      <div
        class="phrase"
        v-for="(review, index) in reviews"
        :key="index"
        v-show="reviewId === index"
      >
        <h3>{{ review.review }}</h3>
        <h6>{{ review.author }}</h6>
      </div>
      <div class="buttons">
        <button :class="selectedButton(0)" @click="changeReview(0)" />
        <button :class="selectedButton(1)" @click="changeReview(1)" />
        <button :class="selectedButton(2)" @click="changeReview(2)" />
      </div>
    </div>
    <PrevNextButton @goBack="PrevReview" @goForward="NextReview" />
    <a href="#">
      <img src="@/assets/data/svg/svg-4.svg" alt="pizza slice" />
    </a>
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
        },
        {
          review: `"THE CRUST IS SO TENDER IT BARELY FIGHTS FORK, KNIFE OR TEETH."`,
          author: "NEW YORK TIMES 2019",
        },
        {
          review: `"PROBABLY THE BEST RESTAURANT IN THE AREA, VERY GOOD AND VERY LIGHT PIZZA, PERFECT WELCOME"`,
          author: "DAILY POST 2020",
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
    selectedButton(x) {
      if (this.reviewId === x) {
        return "selected";
      } else {
        return "notSelected";
      }
    },
    changeReview(x) {
      this.reviewId = x;
    },
    ReviewAutoPlay() {
      this.clock = setInterval(this.NextReview, 7000);
    },
  },
  mounted() {
    this.ReviewAutoPlay();
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
    max-height: 150px;

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

  a {
    align-self: flex-end;
    img {
      width: 20px;
      margin: 30px;
    }
  }
}
.phrase {
  min-height: 80px;
}

button {
  cursor: pointer;
}
</style>