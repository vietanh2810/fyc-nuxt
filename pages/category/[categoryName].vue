<script setup>
const products = [
    {
        name: 'Super Hoodie',
        price: 19,
        imageSrc: 'https://picsum.photos/id/1005/400/250'
    },
    {
        name: 'Super Tshirt',
        price: 14,
        imageSrc: 'https://picsum.photos/id/1005/400/250'
    }
]
</script>

<template>
    <div>
        <h1 class="text-5xl text-center p-5">Catégorie : {{ $route.params.categoryName }}</h1>
        <cards-container class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4">
            <product-card v-for="product in products" 
            :name="product.name" 
            :price="product.price"
            :imageSrc="product.imageSrc" 
            />
        </cards-container>
    </div>
</template>