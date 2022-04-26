<template>
  <header>
    <Nav />
    <img src="@/assets/data/img/h3-rev-img-6.png" alt="pizza slice" />
    <div class="btn-left">
      <h4>PREV</h4>
    </div>
    <div class="btn-right">
      <h4>NEXT</h4>
    </div>
  </header>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  name: "headerComponent",
  components: {
    Nav,
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

h4 {
  color: #d34523;
  margin-bottom: 10px;
}

.btn-right {
  position: absolute;
  top: 50%;
  right: -15px;
  transform: rotate(-90deg);
  border-radius: 50px 50px 0px 0px;
  padding: 15px 10px 0px 10px;
  border: none;
  font-size: 10px;
  width: 60px;
  background-color: white;
}

.btn-left {
  position: absolute;
  left: -15px;
  top: 50%;
  transform: rotate(90deg);
  border-radius: 50px 50px 0px 0px;
  padding: 15px 10px 0px 10px;
  border: none;
  font-size: 10px;
  background-color: white;
  width: 60px;
}
</style>