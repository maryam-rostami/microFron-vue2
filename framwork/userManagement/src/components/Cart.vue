<template>
  <div :class="border">
    <div v-for="tap in cart" :key="tap.beverageName" class="item-cart">
      <img :src="tap.logo" />
      <div class="">
        <p class="font-bold">{{ tap.producerName }}</p>
        <p>{{ tap.beverageName }}</p>
      </div>
    </div>
    <div class="text-right">
      <button type="button" class="btn-checkout" @click="checkout">
        Checkout
      </button>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import store, { addToCart, IStore } from "../store";
import { MFE_BORDER } from "../constants";
import { Beverage } from "../types";

export default defineComponent({
  computed: {
    border: () => MFE_BORDER,
    cart: {
      get() {
        return store.cart;
      },
      set(store) {},
    },
  },
  methods: {
    addToCart(tap: Beverage) {
      addToCart(tap);
    },
    checkout() {
      store.cart = [];
    },
  },
});
</script>
