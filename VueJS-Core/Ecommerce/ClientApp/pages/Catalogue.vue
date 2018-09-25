<template>
    <div>
        <h2>Catalogue</h2>
        <ul v-for="product in products" :key="product.slug">
            <li @click="view(product)">{{ product.name }}</li>
        </ul>
    </div>
</template>

<script>
export default {
  name: "catalogue",
  data() {
    return {
        products: [
          {
              name: "Samsung Galaxy S8",
              slug: "samsung-galaxy-s8"              
          },
          {
              name: "Apple iPhone X",
              slug: "apple-iphone-x"              
          },
          {
              name: "Apple iPhone 5",
              slug: "apple-iphone-5"              
          }
        ]
    }
  },
  methods: {
    view(product) {
      this.$router.push(`/products/${product.slug}`);
    }
  }
};
</script>