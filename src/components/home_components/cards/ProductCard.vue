<template>
    <div class="product__card">
        <img
            :src="image_url"
            :alt="brand"
            class="product__image"
            loading="lazy"
        />
        <div class="product__header">
            <span class="brand">{{ brand }}</span>
        </div>
        <p class="product__name">{{ productName }}</p>
        <div class="price">
            <span>{{ formattedPrice }}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: "ProductCard",
    props: [
        "productId",
        "image_url",
        "brand",
        "productName",
        "price",
        "currency",
    ],
    
};
</script>

<style scoped>
.product__card {
    border: 1px solid var(--grey);
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1);
    transition: transform 0.05s ease-in;
    padding: 15px;
    text-align: left;
    border-radius: 15px;
    color: #222;
}

.product__image {
    height: auto;
    max-width: 100%;
    border-radius: 5px;
}

.product__name {
    padding-block: 10px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.product__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 10px;
}

.brand {
    font-size: 1.5rem;
    display: inline-block;
    font-weight: 700;
}

.price {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.price span {
    font-size: 1.6rem;
    font-weight: 700;
}

</style>
