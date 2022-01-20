<template>
  <div class="catalog">
   catalog page HELLO
    <catalogItem
      v-for="product in this.$store.state.products"
    
      :product_data="product"
      @send-parent="receiveFromChild"
    />
  </div>
</template>
<script>
    //  :key="product.article"
import catalogItem from "./catalogItem.vue";
import {mapActions} from 'vuex'
export default {
  name: "catalog",
  components: { catalogItem },
  data: function () {
    return {
    };
  },
  methods: {
      ...mapActions([
         ' GET_PRODUCTS_FROM_API'
      ])
    receiveFromChild(data) {
      console.log(data);
    },
    mounted(){
this.GET_PRODUCTS_FROM_API()
    }
  },
};
 </script>


<style>
.catalog {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
}
</style>
