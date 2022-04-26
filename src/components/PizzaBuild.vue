<template>
  <section>
    <div class="container">
      <div class="container-text">
        <h1>GO AHEAD AND BUILD YOUR OWN PIZZA WE WON'T JUDGE!</h1>
      </div>
    </div>
    <div class="slice">
      <a href="#">
        <img src="@/assets/data/svg/svg-4.svg" alt="pizza slice" />
      </a>
    </div>
  </section>
</template>

<script>
export default {
  name: "pizzaBuildItem",
};
</script>

<style scoped lang="scss">
section {
  background-image: url(@/assets/data/img/h3-background-img.jpg);
  background-size: fill;
  background-position: center;
  padding: 100px;
  margin-bottom: 10px;
  position: relative;

  .container {
    width: 70%;
    margin: auto;

    .container-text {
      width: 40%;
      margin-top: 30px;
      text-align: left;

      h1 {
        color: white;
        font-size: 50px;
        margin-left: 100px;
      }
    }
  }
  .slice {
    background-color: white;
    width: 40px;
    padding: 7px 0px;
    border-radius: 50%;
    text-align: center;
    position: absolute;
    right: 20px;
    top: 70%;
    img {
      width: 20px;
    }
  }
}
</style>