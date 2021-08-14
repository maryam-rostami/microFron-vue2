<template>
  <div style="width: 100%">
    <h1 class="text-center">User managment</h1>
    <div class="content-mf1">
      <Search />
      <Taps />
      <Cart />
    </div>
  </div>
</template>

<script>
import Taps from "./Taps";
import Search from "./Search";
import Cart from "./Cart";

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
.text-center {
  text-align: center;
}
.user-management {
  padding: 10px;
  background: #ffff0066;
}
</style>
