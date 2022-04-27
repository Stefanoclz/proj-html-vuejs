<template>
  <section>
    <div class="container">
      <form>
        <span class="formInput">
          <input type="text" placeholder="1 person" id="people" />
          <i class="fa-solid fa-user-group"></i>
        </span>
        <h4>FOR</h4>
        <span class="formInput">
          <input type="date" id="date" placeholder="27/04/2022" />
        </span>
        <h4>AT</h4>
        <span class="formInput">
          <input type="time" id="date" />
        </span>
        <input class="button" type="submit" value="BOOK A TABLE" />
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: "formItem",
};
</script>

<style scoped lang="scss">
section {
  background-image: url(@/assets/data/img/h3-background-img-3.jpg);
  margin: 10px 0px;
  padding: 100px 0px;

  .container {
    width: 50%;
    margin: 0 auto;
    display: flex;
    justify-content: center;

    form {
      display: flex;
      align-items: center;
      column-gap: 40px;
      color: white;
      justify-content: center;
    }
  }

  .formInput {
    background-color: white;
    padding: 18px;

    input {
      border: none;
    }
  }
}

.button {
  padding: 22px 60px;
  background-color: #d2401e;
  color: white;
  border: none;
}

i {
  color: black;
  font-size: 13px;
}
</style>