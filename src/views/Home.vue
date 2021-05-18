<template>
  <div class="home">



    <div class="product-cards-container">
      <ProductSummaryCard
      v-for="product in items"
      :key="product.id"
      :product="product"
      />
    </div>
  </div>
</template>

<script>
import items from '../data/items.js'
import ProductSummaryCard from '../components/products/ProductSummaryCard.vue'

export default {
  name: 'Home',
  components: {
      ProductSummaryCard
  },
  data(){
    return {
      items,
    }
  }
}
</script>


<style lang="scss" scoped>
  .product-cards-container{
    display:flex;
    flex-wrap: wrap;
    justify-content: center;
  }
</style>