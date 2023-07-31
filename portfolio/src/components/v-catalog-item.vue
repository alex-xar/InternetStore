<template>
  <div class="v-catalog-item">
    <img
      class="v-catalog-item__image"
      v-bind:src="require('../assets/images/' + product_data.image)"
      alt="img"
    />
    <p class="v-catalog-item__name">{{ product_data.name }}</p>
    <p class="v-catalog-item__prise">{{ product_data.price }} грн.</p>
    <button class="v-catalog-item__btn boton" @click="addToCart">
      <a href="#" class="btn__a"
        ><span class="btn__span">додати до кошика</span></a
      >
    </button>
  </div>
</template>

<script>
export default {
  name: "v-catalog-item",
  props: {
    product_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  data() {
    return {};
  },
  computed: {},
  methods: {
    addToCart() {
      this.$emit("addToCart", this.product_data);
    },
  },
};
</script>

<style lang="scss">
.v-catalog-item {
  flex-basis: 25%;
  box-shadow: 0 0 8px 0 orange;
  padding: 15px;
  margin: 15px;

  &__image {
    width: 100px;
  }
}
</style>
