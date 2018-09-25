<template>
  <div>
    <h2>Product Details</h2>
    <p>{{ productUrl }}</p>
  </div>
</template>

<script>
export default {
  name: "product",
  data() {
    return {
      productUrl: null
    }
  },
  mounted() {
    this.productUrl = this.$route.params.slug;
  }
};
</script>