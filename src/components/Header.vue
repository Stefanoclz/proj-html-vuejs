<template>
  <header>
    <Nav />
    <img
      v-if="sliceId === 1"
      src="@/assets/data/img/h3-rev-img-2.png"
      alt="pizza slice"
    />
    <img
      v-if="sliceId === 2"
      src="@/assets/data/img/h3-rev-img-4.png"
      alt="pizza slice"
    />
    <img
      v-if="sliceId === 3"
      src="@/assets/data/img/h3-rev-img-6.png"
      alt="pizza slice"
    />
    <PrevNextButton @goBack="PrevSlice" @goForward="NextSlice" />
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
  data() {
    return {
      sliceId: 1,
      clock: undefined,
    };
  },
  methods: {
    PrevSlice() {
      this.sliceId--;
      if (this.sliceId < 1) {
        this.sliceId = 3;
      }
    },
    NextSlice() {
      this.sliceId++;
      if (this.sliceId > 3) {
        this.sliceId = 1;
      }
    },
    SliceAutoPlay() {
      this.clock = setInterval(this.NextSlice, 10000);
      console.log(this.sliceId);
    },
  },
  mounted() {
    this.SliceAutoPlay();
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
  max-height: 400px;
}
</style>