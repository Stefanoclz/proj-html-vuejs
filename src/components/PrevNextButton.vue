<template>
  <div>
    <button class="btn-left" @click="prevImage"><h4>PREV</h4></button>
    <button class="btn-right" @click="nextImage"><h4>NEXT</h4></button>
  </div>
</template>

<script>
export default {
  name: "buttonsItem",
  methods: {
    prevImage() {
      this.$emit("goBack");
    },
    nextImage() {
      this.$emit("goForward");
    },
  },
};
</script>

<style scoped lang="scss">
h4 {
  color: #d34523;
  margin-bottom: 10px;
}

button {
  transition: background-color 0.2s ease-in;
}

.btn-right {
  position: absolute;
  top: 50%;
  right: -10px;
  transform: rotate(-90deg);
  border-radius: 50px 50px 0px 0px;
  padding: 15px 10px 0px 10px;
  border: none;
  font-size: 10px;
  width: 60px;
  background-color: white;
}

.btn-left {
  position: absolute;
  left: -10px;
  top: 50%;
  transform: rotate(90deg);
  border-radius: 50px 50px 0px 0px;
  padding: 15px 10px 0px 10px;
  border: none;
  font-size: 10px;
  background-color: white;
  width: 60px;
}

button:hover {
  cursor: pointer;
  background-color: lightgray;
}
</style>