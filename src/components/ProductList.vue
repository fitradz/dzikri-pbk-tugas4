<template>
  <div>
    <ProductItem 
      v-for="product in products" 
      :key="product.id" 
      :product="product"
      @show-detail="showProductDetail"
    />
  </div>
</template>

<script>
import ProductItem from './ProductItem.vue';

export default {
  components: { ProductItem },
  props: ['products'],
  methods: {
    showProductDetail(product) {
      this.$emit('show-detail', product);
    }
  }
};
</script>
<style scoped>
div {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
</style>