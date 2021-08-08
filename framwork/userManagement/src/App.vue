<template>
  <div class="content-mf1">
    <Search />
    <Taps />
    <Cart />
  </div>
</template>

<script>
import Taps from "./components/Taps";
import Search from "./components/Search";
import Cart from "./components/Cart";

export default {
  components: {
    Search,
    Taps,
    Cart,
  },
};
</script>

<style lang="scss">
.content-mf1 {
  width: 100%;
  display: flex;
}
.item {
  padding: 10px;
  border: 3px solid #4fd24f;
  flex-grow: 4;
  margin: 15px;
  text-align: center;
  font-size: 30px;
}
</style>
