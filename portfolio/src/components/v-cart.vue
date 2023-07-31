<template>
  <div class="v-cart">
    <h1>кошик</h1>
    <v-cart-item
      v-for="(item, index) in cart_data"
      v-bind:key="item.article"
      v-bind:cart_item_data="item"
      @deleteFromCart="deleteFromCart(index)"
    />
    <div class="v-cart__total">
      <p class="total__name">Всього</p>
      <p>{{ cartTotalCost }} грн.</p>
    </div>
  </div>
</template>

<script>
import vCartItem from "./v-cart-item.vue";
import { mapActions } from "vuex";
export default {
  name: "v-cart",
  components: { vCartItem },
  props: {
    cart_data: {
      type: Array,
      default() {
        return [];
      },
    },
  },
  data() {
    return {};
  },
  computed: {
    cartTotalCost() {
      let result = [];
      if (this.cart_data.length) {
        for (let item of this.cart_data) {
          result.push(item.price * item.quantity);
        }
        result = result.reduce(function (sum, el) {
          return sum + el;
        });
        return result;
      } else {
        return 0;
      }
    },
  },
  methods: {
    ...mapActions(["DELETE_FROM_CART"]),
    deleteFromCart(index) {
      this.DELETE_FROM_CART(index);
    },
  },
};
</script>

<style lang="scss">
.v-cart {
  &__total {
    padding: 40px;
    display: flex;
    justify-content: center;
    background: #fae7e7;
  }
}
.total__name {
  margin-right: 20px;
}
</style>
