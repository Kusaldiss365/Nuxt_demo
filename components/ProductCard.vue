<template>
    <div>
        <div class="card bg-white text-center p-8 rounded-lg">
            <img :src="product.image" alt="image" class="image">
            <p>Title: {{ product.title }}</p>
            <p>Price: ${{ product.price }}</p>
            <NuxtLink :to="`/products/${product.id}`">
            <p class="btn px-3 py-3 mt-5 items-center justify-center bg-green-400 rounded-lg hover:font-bold">View</p>
            </NuxtLink>
        </div>
    </div>
</template>

<script>
export default{
    props: {
        product: {
            type: Object,
            required: true
        }
    }
}
</script>

<style scoped>
.image{
    max-height: 120px;
    max-width: 70%;
    margin: 0 auto;
}
</style>