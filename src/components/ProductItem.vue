<template>
  <div @click="showDetail">
    <h3>{{ product.name }}</h3>
    <p>{{ product.price }}</p>
  </div>
</template>

<script>
export default {
  props: ['product'],
  methods: {
    showDetail() {
      this.$emit('show-detail', this.product);
    }
  }
};
</script>

<style scoped>
div {
  background-color: #f9f9f9;
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 10px;
  transition: background-color 0.3s ease;
}

div:hover {
  background-color: #f0f0f0;
}

h3 {
  margin: 0 0 5px 0;
}

p {
  margin: 0;
  color: #999;
}
</style>