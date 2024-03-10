<template>
    <main-header />
    <banner-section />
    <about-section />
    <contact-section />
</template>

<script>
import BannerSection from "@/components/home_components/BannerSection.vue";
import FeaturedProducts from "@/components/home_components/products/FeaturedProducts.vue";  
import ActionButton from "@/components/ActionButton.vue";
import MainHeader from "@/components/MainHeader.vue";
import AboutSection from "@/components/home_components/AboutSection.vue";
import ContactSection from "@/components/home_components/ContactSection.vue";

export default {
    name: "HomeView",
    data() {
        return {
            products: [],
        };
    },

    components: {
        BannerSection,
        AboutSection,
        FeaturedProducts,
        ActionButton,
        MainHeader,
        ContactSection,
    },
   
};
</script>
