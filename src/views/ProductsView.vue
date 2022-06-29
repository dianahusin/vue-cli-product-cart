<template>
  <div class="products-view">
    <main class="wrapper">
      <h1>Products</h1>
      <div class="card-container">
         <ProductCard
          v-for="(product, index) in inventory"
          :key="product.id"
          class="card"
          :index="index"
          :product="product"
          :addToCart="addToCart"
        />
      </div>
    </main>
  </div>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue'

export default {
  components: {
    ProductCard
  },
  props: ['inventory', 'addToCart']
}
</script>
