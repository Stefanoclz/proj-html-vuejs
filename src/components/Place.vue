<template>
  <section>
    <div class="card">
      <img src="@/assets/data/img/h3-img-1.jpg" alt="restaurant" />
      <div class="detail">
        <div class="circle">
          <i class="fa-regular fa-eye"></i>
        </div>
      </div>
    </div>
    <div class="card">
      <img src="@/assets/data/img/h3-img-2.jpg" alt="Eat Good Pizza" />
      <div class="detail">
        <div class="circle">
          <i class="fa-regular fa-eye"></i>
        </div>
      </div>
    </div>
    <div class="card">
      <img src="@/assets/data/img/h3-img-3.jpg" alt="Yum" />
      <div class="detail">
        <div class="circle">
          <i class="fa-regular fa-eye"></i>
        </div>
      </div>
    </div>
    <div class="card">
      <img src="@/assets/data/img/h3-img-4.jpg" alt="Bigger pizza" />
      <div class="detail">
        <div class="circle">
          <i class="fa-regular fa-eye"></i>
        </div>
      </div>
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

    .detail {
      width: 100%;
      height: 100%;
      background-image: url(@/assets/data/img/background_dotted.jpg);
      display: none;
      justify-content: center;
      align-items: center;

      .circle {
        padding: 30px;
        background-color: #d2401e;
        border-radius: 50%;
        color: white;

        i {
          font-size: 25px;
        }
      }
    }
  }
}

.card:hover img {
  display: none;
}

.card:hover .detail {
  display: flex;
}
</style>