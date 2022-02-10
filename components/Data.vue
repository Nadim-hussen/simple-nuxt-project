<template>
  <div>
    <h1>Product List</h1>

    <DataCard v-for="product in products" :key="product.id" :data="product" />
    <!-- <div v-for="product in products" :key="product.id">
            <h3>{{product.title}}</h3>

        </div> -->
  </div>
</template>
<script>
export default {
  data() {
    return {
      products: [],
    };
  },
  async fetch() {
    this.products = await fetch(
      "https://jsonplaceholder.typicode.com/posts"
    ).then((res) => res.json());
  },
};
</script>
<style scoped>
h1{
  text-align: center;
}
</style>