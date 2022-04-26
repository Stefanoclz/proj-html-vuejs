<template>
  <section>
    <div class="card">
      <img
        class="foto"
        src="@/assets/data/img/h1-team-1a-700x700.jpg"
        alt="people 1"
      />
      <div class="container">
        <div class="bio">
          <h1>ESTEBAN RODRIGUEZ</h1>
          <p>Manager</p>
          <div class="social">
            <i class="fa-brands fa-instagram-square"></i>
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-facebook-f"></i>
          </div>
        </div>
      </div>
    </div>

    <div class="card">
      <img class="foto" src="@/assets/data/img/h1-team-2a.jpg" alt="people 1" />
      <div class="container">
        <div class="bio">
          <h1>REBECCA PALMER</h1>
          <p>Recruiter</p>
          <div class="social">
            <i class="fa-brands fa-instagram-square"></i>
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-facebook-f"></i>
          </div>
        </div>
      </div>
    </div>

    <div class="card">
      <img class="foto" src="@/assets/data/img/h1-team-4a.jpg" alt="people 1" />
      <div class="container">
        <div class="bio">
          <h1>JASON COOPER</h1>
          <p>Chef</p>
          <div class="social">
            <i class="fa-brands fa-instagram-square"></i>
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-facebook-f"></i>
          </div>
        </div>
      </div>
    </div>

    <div class="card">
      <img class="foto" src="@/assets/data/img/h1-team-3a.jpg" alt="people 1" />
      <div class="container">
        <div class="bio">
          <h1>ESTELLE LAMBERT</h1>
          <p>Chief Operator</p>
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