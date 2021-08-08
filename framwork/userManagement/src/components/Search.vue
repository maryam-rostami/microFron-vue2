<template>
  <div :class="border">
    <h1 class="">Alcohol</h1>
    <input type="range" v-model="alcoholLimit" min="0" max="15" class="" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import store, { setAlcoholLimit } from "../store";
import { MFE_BORDER } from "../constants";

export default defineComponent({
  computed: {
    border: () => MFE_BORDER,
    alcoholLimit: {
      get() {
        return store.alcoholLimit;
      },
      set(value) {
        setAlcoholLimit(value);
      },
    },
  },
});
</script>
