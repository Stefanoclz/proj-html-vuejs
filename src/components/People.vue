<template>
  <section>
    <div class="card" v-for="person in allStaff" :key="person.id">
      <img
        class="foto"
        :src="require(`@/assets/data/img/h1-team-${person.link}.jpg`)"
        alt="people 1"
      />
      <div class="container">
        <div class="bio">
          <h1>{{ person.name }}</h1>
          <p>{{ person.role }}</p>
          <div class="social">
            <i class="fa-brands fa-instagram-square"></i>
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-facebook-f"></i>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "peopleItem",
  data() {
    return {
      allStaff: [
        {
          link: "1a-700x700",
          name: "ESTEBAN RODRIGUEZ",
          role: "Manager",
          id: 1,
        },
        {
          link: "2a",
          name: "REBECCA PALMER",
          role: "Recruiter",
          id: 2,
        },
        {
          link: "3a",
          name: "JASON COOPER",
          role: "Chef",
          id: 3,
        },
        {
          link: "4a",
          name: "ESTELLE LAMBERT",
          role: "Chief Operator",
          id: 4,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
section {
  display: flex;

  .card {
    width: calc(100% / 4);
    height: 400px;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: top;
    }
  }
  .container {
    width: 100%;
    height: 100%;
    margin: 0 auto;
    display: none;
    background-color: #d2401e;
    align-self: center;
  }
  .bio {
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    row-gap: 20px;
    align-items: center;
    width: 100%;
    margin: auto;

    .social {
      display: flex;
      column-gap: 10px;
    }
  }
}

.card:hover img {
  display: none;
}
.card:hover .container {
  display: flex;
}
</style>