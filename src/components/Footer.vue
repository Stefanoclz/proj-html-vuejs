<template>
  <footer>
    <Form />
    <div class="bot-footer">
      <div class="info">
        <div class="container">
          <div class="links">
            <div class="findUs">
              <h3>FIND OUR RESTAURANTS</h3>

              <div>
                <p>1614 E. Bell Rd #104.</p>
                <p>Salerno, AZ 58022</p>
                <p>(602)867-1010</p>
              </div>

              <div>
                <p>204 E. Pizzetta Tommaso</p>
                <p>Salerno, AZ 58022</p>
                <p>(358)867-1010</p>
              </div>

              <div>
                <p>Vale Puglia 54</p>
                <p>Torre Del Greco, AZ 58022</p>
                <p>(359)867-1010</p>
              </div>

              <div>
                <p>Corso Itali AA</p>
                <p>Naples, AZ 58022</p>
                <p>(989)867-1010</p>
              </div>
            </div>
            <div class="hours">
              <h3>WORKING HOURS</h3>
              <div>
                <h5>MONDAY</h5>
                <h6>Kitchen Closed</h6>
              </div>

              <div>
                <h5>TUSEDAY UNTIL FRIDAY</h5>
                <p>9:00 - 22:00</p>
              </div>

              <div>
                <h5>SATURDAY</h5>
                <p>Saturday 11am to midnight</p>
              </div>

              <div>
                <h5>SUNDAY</h5>
                <p>09:00 - 22:00</p>
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
};
</script>

<style scoped lang="scss">
.bot-footer {
  display: flex;
  background-color: #1b1b1b;
  color: white;
  text-align: left;
  margin-bottom: 0px;

  .info {
    display: flex;
    flex-direction: column;
    width: calc(100% / 2);

    .links {
      display: flex;
      column-gap: 100px;

      .findUs,
      .hours {
        display: flex;
        flex-direction: column;
        row-gap: 20px;

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
  margin: 150px auto;
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