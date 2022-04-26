<template>
  <div>
    <div class="btn-left">
      <h4>PREV</h4>
    </div>
    <div class="btn-right">
      <h4>NEXT</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "buttonsItem",
};
</script>

<style scoped lang="scss">
h4 {
  color: #d34523;
  margin-bottom: 10px;
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
</style>