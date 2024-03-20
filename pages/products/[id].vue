<template>
    <div class="card">
      <div class="grid grid-cols-2 gap-10">
        <ProductDetails :product="product" />
      </div>
    </div>
  </template>
  
  <script>
  import ProductDetails from '~/components/ProductDetails.vue';

  export default {

    data(){
      return{
        product: {}
      }
    },
    
    methods: {
      async loadData() {
      try {
        const { id } = useRoute().params;
        const url = `https://fakestoreapi.com/products/${id}`;
        const response = await fetch(url);
        const product = await response.json();
        this.product = product;
      } catch (error) {
        console.error('Error fetching product:', error);
        return { product: null };
      }
    }},
    components: {
        ProductDetails
    },
    mounted(){
      this.loadData();
    }
  }
  </script>
  
  
  <style scoped>
  </style>
  