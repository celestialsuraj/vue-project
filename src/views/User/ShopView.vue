<template>
    <main-header />
    <div class="container">
        <div class="product__container" >
            <product-card
                v-for="(product, index) in products"
                :key="index"
                :productId="product._id"
                :productName="product.name"
                :brand="product.brand"
                :price="product.price"
                :currency="product.currency"
                :ratings="product.rating"
                :image_url="product.images[0]"
                :in_stock="product.in_stock"
            />
        </div>
    </div>
</template>

<script>
import ProductCard from "@/components/home_components/cards/ProductCard.vue";
import { products } from "@/data";
import MainHeader from "@/components/MainHeader.vue";

export default {
    name: "ShopView",
    components: {
        ProductCard,
        MainHeader,},
    data() {
        return {
            products,
        };
    },
};
</script>

<style>
.product__container{
    display: grid;
    grid-template-columns: repeat(4,2fr);
    gap: 20px;
    /* display: flex; */
}

</style>
