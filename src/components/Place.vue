<template>
  <section>
    <div class="card">
      <img src="@/assets/data/img/h3-img-1.jpg" alt="restaurant" />
    </div>
    <div class="card">
      <img src="@/assets/data/img/h3-img-2.jpg" alt="Eat Good Pizza" />
    </div>
    <div class="card">
      <img src="@/assets/data/img/h3-img-3.jpg" alt="Yum" />
    </div>
    <div class="card">
      <img src="@/assets/data/img/h3-img-4.jpg" alt="Bigger pizza" />
    </div>
  </section>
</template>

<script>
export default {
  name: "placeItem",
};
</script>

<style scoped lang="scss">
section {
  width: 100%;
  display: flex;
  justify-content: space-between;
  margin: 10px 0px;
  column-gap: 10px;
  .card {
    width: calc(100% / 4);
    img {
      width: 100%;
    }
  }
}
</style>