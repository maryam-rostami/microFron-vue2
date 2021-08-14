<template>
  <div class="text-3xl font-bold">
    <header>Menu</header>
    <div class="p-10">
      <h1>MF 1</h1>

      <div class="content">
        <div class="content-body">
          <h3>Components can be used independently</h3>
          <div class="content-grid">
            <Search />
            <Cart />
          </div>
        </div>

        <div class="content-body">
          <h3>The whole module can be used in one place</h3>
          <div class="content-grid">
            <UserManagement />
          </div>
        </div>
      </div>
    </div>

    <hr />

    <div class="p-10">
      <h1>MF 2</h1>

      <div class="content">
        <div class="content-body">
          <div class="content-grid"></div>
        </div>

        <div class="content-body">
          <div class="content-grid"></div>
        </div>
      </div>
    </div>
    <footer>Footer</footer>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import Search from "whatever/Search";
import Taps from "whatever/Taps";
import Cart from "whatever/Cart";
import UserManagement from "whatever/UserManagement";

export default defineComponent({
  components: {
    Search,
    Taps,
    Cart,
    UserManagement,
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
body {
  margin: 0;
  padding: 0;
}
.p-10 {
  padding: 10px;
}
</style>
