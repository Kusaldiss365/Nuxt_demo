
<template>
<h1 class="text-xl mt-8 ms-10 font-semibold">Products</h1>
        <div class="grid m-10 2xl:grid-cols-4 sm:grid-cols-2 lg:grid-cols-3 gap-4">
            <div v-for="p in products" :key="p.id">
                <ProductCard :product="p"/>
            </div>
        </div>
</template>

<script>
import ProductCard from '~/components/ProductCard.vue';

export default{

  data(){
    return{
      products: []
    }
    },

    components: {
        ProductCard
    },
    
    async fetch() {
    console.log(1)
    await this.$axios.$get("https://fakestoreapi.com/products")
      .then((response) => {
        this.products = response;
        console.log(response)
      })
      .catch((error) => {
        console.error("Error: ", error.message);
      });
    },

      // methods: {
    //   async loadData() {
    //   try {
    //       const response = await fetch('https://fakestoreapi.com/products');
    //       const products = await response.json();
    //       this.products = products;
    //   } catch (error) {
    //     console.error('Error fetching products:', error);
    //   }
    //   }
    // },

    // mounted(){
    //   this.loadData();
    // }

}
</script>

<style scoped>
</style>