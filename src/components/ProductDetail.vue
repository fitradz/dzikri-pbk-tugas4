<template>
  <div v-if="product">
    <h2>{{ product.name }}</h2>
    <p>{{ product.description }}</p>
    <p>{{ product.price }}</p>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: ['product']
};
</script>
<style scoped>
div {
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 20px;
  margin-top: 20px;
}

h2 {
  margin: 0 0 10px 0;
}

p {
  margin: 5px 0;
  color: #555;
}
</style>