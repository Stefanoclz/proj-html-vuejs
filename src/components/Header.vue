<template>
  <header>
    <Nav />
  </header>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  name: "headerComponent",
  components: {
    Nav,
  },
};
</script>

<style scoped lang="scss">
header {
  background-color: rgba($color: #000000, $alpha: 0.9);
  color: white;
  padding: 20px 0px;
}
</style>