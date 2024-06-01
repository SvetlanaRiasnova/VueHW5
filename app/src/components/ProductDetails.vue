<template>
  <div>
    <h1>OUR PRODUCTS</h1>
    <div class="prod_container">
      <div v-for="(item, index) in product" :key="index" class="product_item">
        <p>name: {{ item.name }}</p>
        <p>price: {{ newPrice(item.price) }}</p>
        <p v-if="item.available">Available</p>
        <p v-else>Out of stock</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductDetails",

  data() {
    return {
      price: "",
      product: [
        {
          name: "Milk",
          price: 99.99,
          available: true,
        },
        {
          name: "Juece J7",
          price: 33.99,
          available: true,
        },
        {
          name: "Bread",
          price: 0.99,
          available: true,
        },
        {
          name: "Oil",
          price: 9.45,
          available: false,
        },
      ],
    };
  },

  computed: {
    newPrice() {
      return (price) => `$${price}`;
    },
  },
};
</script>

<style scoped lang="scss">
.prod_container {
  display: flex;
  justify-content: center;
  font-size: 24px;
  gap: 60px;
}
.product_item {
  border: 2px solid #9f9f9f;
  padding: 10px;
  background-color: aquamarine;
}
</style>
