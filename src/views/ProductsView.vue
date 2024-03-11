
<template>
<main class="wrapper">
  <h1>Products</h1>

  <div class="card-container">
    <ProductCard
      v-for="(product, index) in inventory.slice(0,9)"
      :key="product.id"
      :index="index"
      :product="product"
      :addToCart="addToCart"
        />
  </div>
</main>
</template>
<script>
import ProductCard from '@/components/ProductCard'
export default {
  name: 'ProductView',
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>
