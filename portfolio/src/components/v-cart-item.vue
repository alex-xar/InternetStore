<template>
  <div class="v-cart-item">
    <img
      class="v-cart-item__image"
      v-bind:src="require('../assets/images/' + cart_item_data.image)"
      alt="img"
    />
    <div class="v-cart-item-info">
      <p>{{ cart_item_data.name }}</p>
      <p>{{ cart_item_data.price }}</p>
      <p>{{ cart_item_data.article }}</p>
    </div>
    <div class="v-cart-item__quantity">
      <P>Кількість</P>
      {{ cart_item_data.quantity }}
    </div>
    <button @click="deleteFromCart" class="boton v-cart-item__btn">
      <a href="#" class="btn__a"
        ><span class="btn__span">Забрати з кошика</span></a
      >
    </button>
  </div>
</template>

<script>
export default {
  name: "v-cart-item",
  props: {
    cart_item_data: {
      type: Object,
      Default() {
        return {};
      },
    },
  },
  data() {
    return {};
  },
  computed: {},
  methods: {
    deleteFromCart() {
      this.$emit("deleteFromCart");
    },
  },
  mounted() {
    const cartItemData = this.cart_item_data;
    cartItemData.quantity = 1;
  },
};
</script>

<style lang="scss">
.v-cart-item {
  display: flex;
  flex-wrap: nowrap;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0 0 8px 0 orange;
  padding: 20px;
  margin: 20px;
  &__image {
    max-width: 100px;
  }
}
</style>
