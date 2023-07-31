<template>
  <vHeader />
  <div class="v-main-wrapper">
    <vCatalog />
    <vCart v-bind:cart_data="CART" />
  </div>
  <vFooter />
</template>

<script>
import vFooter from "./v-footer.vue";
import vHeader from "./v-header.vue";
import vCatalog from "./v-catalog.vue";
import vCart from "./v-cart.vue";
import { mapGetters } from "vuex";

export default {
  name: "v-main-wrapper",
  components: { vCatalog, vCart, vHeader, vFooter },
  props: {},
  computed: {
    ...mapGetters(["CART"]),
  },
  methods: {},
  watch: {},
  mounted() {
    console.log("hello");
  },
};
</script>

<style lang="scss">
.v-main-wrapper {
  max-width: 900px;
  margin: 0 auto;
  font-weight: bold;
}
</style>
