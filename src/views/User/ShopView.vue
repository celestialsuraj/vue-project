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
.btn {
    border: none;
    background-color: #f2f2f2;
    padding-inline: 20px;
    height: 40px;
    border: 2px solid var(--grey-2);
    font-size: 1.7rem;
    margin-inline: 5px;
    cursor: pointer;
}

.back-btn,
.next-btn {
    background-color: #f2f2f2;
    color: black;
}

.btn:hover {
    background-color: #083e46;
    border-color: #083e46;
    color: white;
}

.btn-active {
    background-color: #083e46;
    color: white;
    border-color: #083e46;
}

.pagination {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 2rem 0;
}
</style>
