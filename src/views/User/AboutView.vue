<template>
    <main-header />
    <div class="container">
        <article>
            <img
                src="@/assets/images/a6.webp"
                class="about-img"
                alt="Who we are"
            />
            <div class="about-text">
                <h1>Who We Are ?</h1>
                <p>
                    We pride ourselves to our delivery time and customer
                    satisfaction first approach. Our platform connects you to
                    the best service providers in your area. We are a team of
                    young and passionate individuals who are dedicated to
                    providing you with the best service possible.
                </p>
            </div>
        </article>
        <div class="video-section">
            <h1>Download Our <a href="/">App</a></h1>
            <img
                src="@/assets/images/download.svg"
                alt=""
                class="video-banner"
            />
        </div>
    </div>
</template>

<script>
import MainHeader from "@/components/MainHeader.vue";
export default {
    components: { MainHeader, },
    name: "AboutView",
};
</script>

<style scoped>
article {
    display: flex;
    gap: 4rem;
    margin-bottom: 2.5rem;
}
.about-img {
    margin-top: 5rem;
    height: 50vh;
    width: 50%;
    object-fit: cover;
}

.about-text {
    margin-top: 5rem;
    width: 50%;
}

.about-text p {
    line-height: 25px;
}

.video-section {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding-block: 3rem;
    text-align: center;
}

.video-banner {
    height: 60vh;
    width: 60%;
    border-radius: 10px;
    margin-top: 2rem;
}

.video-section a {
    text-decoration: underline;
    color: var(--dark-blue);
}

@media (max-width: 499px) {
    article {
        flex-direction: column;
    }
    .about-img,
    .about-text,
    .video-banner {
        width: 100%;
    }

    h1 {
        font-size: 4rem;
    }
}
</style>
