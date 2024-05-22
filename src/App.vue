<template>
  <div id="app">
    <ProductList :products="products" @show-detail="displayProductDetail" />
    <ProductDetail :product="selectedProduct">
      <template v-slot>
        <p>Harga Sudah Tertera Dari Pabrik</p>
      </template>
    </ProductDetail>
  </div>
</template>

<script>
import ProductList from './components/ProductList.vue';
import ProductDetail from './components/ProductDetail.vue';

export default {
  components: {
    ProductList,
    ProductDetail
  },
  data() {
    return {
      products: [
        { id: 1, name: 'Produk Minyak Goreng', description: 'Kelapa sawit (Elaeis guineensis) yang ditanam di Indonesia merupakan tanaman asli dari Afrika Barat dan Afrika Tengah. Sejarah kelapa sawit yang masuk ke Indonesia pada tahun 1848, berawal dari empat biji kelapa sawit yang dibawa oleh Dr. D. T. Pryce, masing-masing dua benih dari Bourbon, Mauritius dan dua benih lainnya berasal dari Hortus Botanicus, Amsterdam, Belanda.', price: 'Harga = Rp 100.000' },
        { id: 2, name: 'Produk Minyak Kelapa', description: 'Minyak kelapa terkenal memiliki manfaat untuk menjaga kesehatan rambut dan kulit kepala. Sebuah studi tahun 2015 menemukan bahwa penggunaan minyak kelapa sebelum dan sesudah keramas mengurangi hilangnya protein pada rambut. Penelitian lain pada tahun 2021 mengungkapkan bahwa mengoleskan minyak ke kulit kepala dapat mengurangi ketombe.', price: 'Harga = Rp 150.000' }
      ],
      selectedProduct: null
    };
  },
  methods: {
    displayProductDetail(product) {
      this.selectedProduct = product;
    }
  }
};
</script>
<style>
#app {
  font-family: 'Arial, sans-serif';
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

h2, h3 {
  color: #333;
}

p {
  color: #666;
}
</style>