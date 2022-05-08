<template>
  <div>
    <div>
      <input v-model="productId" type="text" >
      <button @click="onLoadProduct">Load product</button>
    </div>
    <div>
      <nuxt-link to="/products/1">product1</nuxt-link>
      <br>
      <nuxt-link to="/products/2">product2</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductsIndex",
  data() {
    return {
      productId: '',
    };
  },
  methods: {
    onLoadProduct() {
      this.$router.push('/products/' + this.productId)
    }
  }
}
</script>

<style scoped>

</style>