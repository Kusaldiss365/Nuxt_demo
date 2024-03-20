<template>
        <div class="p-7">
            <img :src="product.image" alt="Image">
        </div>
        <div class="">
            <h2 class="text-4xl my-7">Title: {{ product.title }}</h2>
            <p class="text-xl my-7">price :  {{ product.price }}</p>
            <h3 class="text-lg my-7">description : </h3>
            <p class="my-7 me-5">{{ product.description }}</p>
            <button class="bg-green-300 px-4 py-3 mt-3 rounded-md hover:font-bold">Add to Cart</button>
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

<style lang="scss" scoped>

</style>