<template>
  <nav>
    <div class="left-nav">
      <button>ORDER ONLINE</button>
    </div>
    <div class="mid-nav">
      <ul>
        <li>
          <a href="#"
            ><img src="@/assets/data/svg/svg-0.svg" alt="baffo" /> HOME</a
          >
        </li>
        <li><a href="#">PAGES</a></li>
        <li><a href="#">MENU</a></li>
      </ul>
      <img
        class="logo"
        src="@/assets/data/img/h5-logo-divided-header.png"
        alt="Don Peppe"
      />
      <ul>
        <li><a href="#">EVENT</a></li>
        <li><a href="#">BLOG</a></li>
        <li><a href="#">LANDING</a></li>
      </ul>
    </div>
    <div class="right-nav">
      <ul>
        <li>
          <a href="#"
            ><img src="@/assets/data/svg/svg-1.svg" alt="cart" /> CART</a
          >
        </li>
        <li>
          <a href="#"><i class="fa-solid fa-magnifying-glass"></i>SEARCH</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "navItem",
};
</script>

<style scoped lang="scss">
nav {
  display: flex;
  justify-content: center;
  column-gap: 10px;
  width: 80%;
  margin: 0 auto;
  font-size: 14px;
  ul {
    list-style-type: none;
    li {
      display: inline-block;
      margin: 0px 15px;

      a {
        text-decoration: none;
        color: white;
      }

      img {
        width: 20px;
        filter: invert(100%);
        margin: 0px 5px;
      }
      i {
        transform: scaleX(-1);
        margin: 0px 5px;
      }
    }
  }
}

.left-nav {
  button {
    background-color: #d2401e;
    color: white;
    padding: 10px 15px;
    border: none;
  }
}

.mid-nav,
.right-nav,
.left-nav {
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo {
  width: 15%;
  margin: 0px 10px;
}
</style>