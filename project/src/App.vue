<template>
  <div class="text-3xl font-bold">
    <header>Menu</header>
    sample project
    <div class="content">
      <div class="content-body">
        <h1>MF 1</h1>
        <div class="content-grid">
          <Search />
          <Taps />
          <Cart />
        </div>
      </div>

      <div class="content-body">
        <h1>MF 2</h1>
        <div class="content-grid"></div>
      </div>
    </div>

    <footer>Footer</footer>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Search from "whatever/Search";
import Taps from "whatever/Taps";
import Cart from "whatever/Cart";

export default defineComponent({
  components: {
    Search,
    Taps,
    Cart,
  },
});
</script>
<style>
header,
footer {
  width: 100%;
  padding: 20px;
  color: #fff;
  background: rgb(29, 5, 75);
}
.content {
  display: flex;
}
.content-grid {
  display: flex;
}
.content-body {
  margin: 15px;
  width: 50%;
  padding: 20px;
  background: #e2e2e2;
}
/* module style  */
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
