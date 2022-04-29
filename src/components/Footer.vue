<template>
  <footer>
    <Form />
    <div class="bot-footer">
      <div class="info">
        <div class="container">
          <div class="links">
            <div class="findUs">
              <h3>FIND OUR RESTAURANTS</h3>

              <div v-for="(info, index) in allRestaurants" :key="index">
                <p>{{ info.address }}</p>
                <p>{{ info.country }}</p>
                <p>{{ info.phone }}</p>
              </div>
            </div>
            <div class="hours">
              <h3>WORKING HOURS</h3>
              <div v-for="(day, index) in workinHours" :key="index">
                <h5>{{ day.day }}</h5>
                <h6>{{ day.detail }}</h6>
              </div>

              <div class="social">
                <h5>FOLLOW US:</h5>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-instagram-square"></i>
                <i class="fa-brands fa-linkedin-in"></i>
              </div>
            </div>
            <h2>
              THE DON PEPPE CREW FIRST AND FOREMOST VALUES AND AUTHENTIC, WELL
              BAKED SLICE OF PIZZA.
            </h2>
          </div>
        </div>

        <div class="credits">
          <div class="container-credits">
            <p>Created with <i class="fa-solid fa-heart"></i> by SC</p>
          </div>
        </div>
      </div>

      <img src="@/assets/data/img/footer-img-1.jpg" alt="old time restaurant" />
    </div>
  </footer>
</template>

<script>
import Form from "@/components/Form.vue";

export default {
  name: "FooterComponent",
  components: {
    Form,
  },
  data() {
    return {
      allRestaurants: [
        {
          address: "1614 E. Bell Rd #104.",
          country: "Salerno, AZ 58022",
          phone: "(602)867-1010",
        },
        {
          address: "204 E. Pizzetta Tommaso",
          country: "Salerno, AZ 58022",
          phone: "(358)867-1010",
        },
        {
          address: "Vale Puglia 54",
          country: "Torre Del Greco, AZ 58022",
          phone: "(359)867-1010",
        },
        {
          address: "Corso Itali AA",
          country: "Naples, AZ 58022",
          phone: "(989)867-1010",
        },
      ],
      workinHours: [
        {
          day: "MONDAY",
          detail: "Kitchen Closed",
        },
        {
          day: "TUSEDAY UNTIL FRIDAY",
          detail: "9:00 - 22:00",
        },
        {
          day: "SATURDAY",
          detail: "Saturday 11am to midnight",
        },
        {
          day: "SUNDAY",
          detail: "09:00 - 22:00",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.bot-footer {
  display: flex;
  background-image: url(@/assets/data/img/sfondo3.jpg);
  color: white;
  text-align: left;
  margin-bottom: 0px;

  .info {
    display: flex;
    flex-direction: column;
    width: calc(100% / 2);

    .links {
      display: flex;
      column-gap: 120px;

      .findUs,
      .hours {
        display: flex;
        flex-direction: column;
        row-gap: 20px;
        width: 250px;

        h3,
        h5 {
          color: #b7903c;
        }

        h6 {
          color: #a9381d;
        }
      }

      h2 {
        margin: 0px 40px;
      }
      p {
        font-size: 15px;
      }
    }

    .credits {
      display: flex;
    }
  }

  img {
    width: calc(100% / 2);
    object-fit: fill;
  }
}

.social {
  display: flex;
  column-gap: 10px;

  i {
    font-size: 13px;
  }
}

.container {
  width: 85%;
  margin: 150px auto 80px auto;
}

.container-credits {
  width: 85%;
  margin: 40px auto 30px auto;
}

.credits {
  display: flex;
  justify-content: space-between;
  font-size: 12px;
  color: #8e7133;
}
</style>