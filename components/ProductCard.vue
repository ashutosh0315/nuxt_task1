<template>
    <div class="product-card">
      <nuxt-link :to="`/product/${product.id}`">
        <img :src="product.image" alt="Product image" />
        <h3>{{ product.title }}</h3>
      </nuxt-link>
      <p><strong>Price:</strong> ${{ product.price }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      product: {
        type: Object,
        required: true
      }
    }
  }
  </script>
  
  <style>
  .product-card {
    border: 1px solid #ccc;
    padding: 20px;
    margin: 10px;
    text-align: center;
  }
  .product-card img {
    max-width: 100%;
    height: auto;
  }
  </style>
  