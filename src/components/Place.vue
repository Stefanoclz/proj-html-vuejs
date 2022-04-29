<template>
  <section>
    <div class="card" v-for="element in images" :key="element.id">
      <img
        :src="require(`@/assets/data/img/h3-img-${element.id}.jpg`)"
        :alt="element.alt"
      />
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
  data() {
    return {
      images: [
        {
          id: "1",
          alt: "restaurant",
        },
        {
          id: "2",
          alt: "Eat Good Pizza",
        },
        {
          id: "3",
          alt: "Yum",
        },
        {
          id: "4",
          alt: "Bigger pizza",
        },
      ],
    };
  },
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

        & {
          cursor: pointer;
        }

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