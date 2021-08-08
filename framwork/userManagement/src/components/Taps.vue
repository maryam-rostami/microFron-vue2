<template>
  <div :class="border">
    <div v-for="tap in filteredTaps" :key="tap.beverageName" class="item-cart">
      <img :src="tap.logo" class="" />
      <div>
        <p class="">
          <span class="font-bold">{{ tap.producerName }}</span>
          {{ tap.beverageName }}
        </p>
        <p class="">
          {{ tap.beverageStyle }} - {{ tap.abv }}% {{ tap.ibu }} IBU
        </p>
        <div class="text-right">
          <button type="button" class="btn-addToCart" @click="addToCart(tap)">
            Add To Cart
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import store, { addToCart } from "../store";
import { MFE_BORDER } from "../constants";
import { Beverage } from "../types";

export default defineComponent({
  computed: {
    border: () => MFE_BORDER,
    filteredTaps: {
      get() {
        return store.filteredTaps;
      },
      set(list) {},
    },
  },
  methods: {
    addToCart(tap: Beverage) {
      addToCart(tap);
    },
  },
});
</script>
