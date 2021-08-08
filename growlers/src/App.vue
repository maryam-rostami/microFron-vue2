<template>
  <div class="content-mf1">
    <Search />
    <Taps />
    <Cart />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Taps from "./components/Taps";
import Search from "./components/Search";
import Cart from "./components/Cart";

export default defineComponent({
  components: {
    Search,
    Taps,
    Cart,
  },
});
</script>
<style lang="scss">
.btn-addToCart {
  padding: 10px;
  font-size: 13px;
  border-radius: 5px;
  background: #3b82f6;
  color: #fff;
  border: 1px solid #3b82f6;
}
button.btn-checkout {
  padding: 20px;
  border: 1px solid green;
  background: green;
  color: #fff;
  display: block;
  width: 100%;
  border-radius: 5px;
  font-size: 20px;
}
.content-mf1 {
  width: 100%;
  display: flex;
}
.item {
  padding: 10px;
  border: 3px solid #4fd24f;
}
.item-cart {
  text-align: center;
  margin-bottom: 15px;
  padding: 15px;
  border-bottom: 1px solid #ccc;
}
</style>
