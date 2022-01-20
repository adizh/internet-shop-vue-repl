<template>
  <div class="MainWrapper">
      {{title}}
      HELLO
 
       <cart /> 
  
  </div>
</template>

<script>
//import catalog from "./catalog.vue";
 import cart from "./cart.vue";
export default {
  name: "MainWrapper",
  components: {cart},
  props: {},
  data: function () {
    return {
      title: "Main page",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
