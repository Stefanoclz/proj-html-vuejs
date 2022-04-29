<template>
  <nav>
    <div class="left-nav">
      <button>ORDER ONLINE</button>
    </div>
    <div class="mid-nav">
      <ul>
        <li v-for="(item, index) in firstList" :key="index">
          <a href="#"
            ><img
              src="@/assets/data/svg/svg-0.svg"
              alt="baffo"
              v-if="item.thereIsImg === true"
            />
            {{ item.value }}</a
          >
        </li>
      </ul>
      <img
        class="logo"
        src="@/assets/data/img/h5-logo-divided-header.png"
        alt="Don Peppe"
      />
      <ul>
        <li v-for="(item, index) in secondList" :key="index">
          <a href="#">{{ item.value }}</a>
        </li>
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
          <input
            type="text"
            placeholder="Search"
            v-if="onSearch"
            @mouseleave="hideTextBar"
          />
          <a href="#" v-else @click="showTextBar"
            ><i class="fa-solid fa-magnifying-glass"></i>SEARCH</a
          >
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "navItem",
  data() {
    return {
      onSearch: false,
      firstList: [
        {
          value: "HOME",
          thereIsImg: true,
        },
        {
          value: "PAGES",
          thereIsImg: false,
        },
        {
          value: "MENU",
          thereIsImg: false,
        },
      ],
      secondList: [
        {
          value: "EVENT",
        },
        {
          value: "BLOG",
        },
        {
          value: "LANDING",
        },
      ],
    };
  },
  methods: {
    showTextBar() {
      this.onSearch = true;
    },
    hideTextBar() {
      this.onSearch = false;
    },
  },
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

      input {
        width: 80px;
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
    cursor: pointer;

    &:hover {
      background-color: crimson;
      transition: 0.5s ease-in;
    }
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

a:hover {
  color: yellowgreen;
}
</style>