<template>
  <section>
    <div class="date">
      <div class="container">
        <h5 class="evidence">MADE WITH LOVE</h5>
        <h2>DELISH PIZZA DEALS</h2>
        <div
          v-for="(item, index) in places"
          :key="index"
          :class="separator(index)"
        >
          <div class="day">
            <h2 class="evidence">{{ item.day }}</h2>
            <h4>{{ item.month }}</h4>
          </div>
          <div class="where">
            <h4>{{ item.place }}</h4>
            <p class="evidence">
              <i class="fa-solid fa-location-dot"></i>{{ item.address }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="comic">
      <img src="@/assets/data/img/h3-img-5a.jpg" alt="comic" />
    </div>
  </section>
</template>

<script>
export default {
  name: "eventsItem",
  data() {
    return {
      places: [
        {
          day: "02",
          month: "NOV",
          place: "TRADITIONAL NEAPOLITAN PIES IN KYOTO PIZZA MERCATO",
          address: "204 E. Pizzetta Tommaso",
        },
        {
          day: "03",
          month: "NOV",
          place: "TERRAZZA PATIO DINING SPACE OPENING THIS WEEKEND",
          address: "204 E. Pizzetta Tommaso",
        },
        {
          day: "05",
          month: "NOV",
          place: "SIENNA PRIVATE DINING ROOM WITH STÈPHANE BRUNN",
          address: "204 E. Pizzetta Tommaso",
        },
      ],
    };
  },

  methods: {
    separator(index) {
      const id = index;
      console.log(id);
      if (id === 0 || id === 2) {
        return "eventName";
      } else {
        return "divide";
      }
    },
  },
};
</script>

<style scoped lang="scss">
section {
  display: flex;

  h5 {
    font-size: 13px;
  }

  h2 {
    font-size: 35px;
  }

  p {
    font-size: 12px;
  }

  .date {
    width: calc(100% / 2);
    background-color: #1a1a1a;
    padding: 100px 0px;
    height: 100%;

    .container {
      width: 45%;
      margin: 40px auto;
      display: flex;
      flex-direction: column;
      row-gap: 20px;
      text-align: left;
      color: white;

      .divide {
        display: flex;
        column-gap: 20px;
        border-bottom: 1px dotted #b18b3b;
        border-top: 1px dotted #b18b3b;
        padding: 30px 0px;
      }

      .eventName {
        display: flex;
        column-gap: 20px;

        .day {
          display: flex;
          flex-direction: column;
        }

        .where {
          display: flex;
          flex-direction: column;
        }
      }
    }
  }

  .evidence {
    color: #a7371d;
  }

  .comic {
    width: calc(100% / 2);
    height: 80vh;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
}
</style>