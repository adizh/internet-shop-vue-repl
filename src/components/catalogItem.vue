<template>
  <div class="catalogItem">
   <!--  <img alt="img" src="product_data.image" /> -->

    <p class="v-catalog-item__name">{{ product_data.name }}</p>
    <p class="v-catalog-item__price">Price: {{ product_data.price }} Р.</p>
    <p class="v-catalog-item__price">{{ product_data.category }}</p>
    <button @click="sendToParent">add to cart</button>
  </div>
</template>
<script>
export default {
  name: "catalogItem",
  components: {},
  props: {
    product_data: {
      type: Object,
      default: null,
    },
  },
  data: function () {
    return {
      title: "catalog item",
    };
  },

  computed: {},

  methods: {
    sendToParent() {
      this.$emit("send-parent", this.product_data.name);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.catalogItem {
  flex-basis: 25%;
  box-shadow: 0 0 8px 0 #e0e0e0;
  padding: 8px;
  margin-bottom: 8px;
}
.v-catalog-item__image {
  width: 100px;
}
</style>
