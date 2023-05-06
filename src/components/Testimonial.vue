<template>
    <section class="container-fluid main-wrapper bg-testimonial">
        <div class="card mb-5 border-0 bg-transparent text-center">
            <p class="card-text"><i class="text-white">Testimonial</i></p>
            <h2 class="card-title text-white fw-bold">Happy Clients</h2>
        </div>
        <div id="carouselExampleCaptions" class="carousel slide">
            <div class="carousel-inner">
                <div class="carousel-item active">
                    <div class="row g-4">
                        <TestimonialItem v-for="(item, index) in carousel1" :key="index" :image="item" />
                    </div>
                </div>
                <div class="carousel-item">
                    <img src="images/person_1.jpg" class="d-block w-100" alt="...">
                    <div class="carousel-caption d-none d-md-block">
                        <h5>Second slide label</h5>
                        <p>Some representative placeholder content for the second slide.</p>
                    </div>
                </div>
                <div class="carousel-item">
                    <img src="..." class="d-block w-100" alt="...">
                    <div class="carousel-caption d-none d-md-block">
                        <h5>Third slide label</h5>
                        <p>Some representative placeholder content for the third slide.</p>
                    </div>
                </div>
            </div>
            <div class="carousel-indicators">
                <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active"
                    aria-current="true" aria-label="Slide 1"></button>
                <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1"
                    aria-label="Slide 2"></button>
                <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2"
                    aria-label="Slide 3"></button>
                <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="3"
                    aria-label="Slide 4"></button>
                <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="4"
                    aria-label="Slide 5"></button>
            </div>
        </div>
        <div>

        </div>
    </section>
</template>

<script>
import TestimonialItem from './TestimonialItem.vue';

export default {
    components: {TestimonialItem},

    data() {
        return {
            carousel1: ['1', '2', '3'],
            carousel2: ['2', '3', '1'],
            carousel3: ['3', '1', '2'],
            carousel4: ['3', '2', '1'],
            carousel5: ['2', '1', '3']
        }
    }
}
</script>

<style scoped>
.bg-testimonial {
    background: url('/images/bg_4.jpg') fixed;
    background-size: cover;
    background-color: rgba(0, 0, 0, 0.377);
    background-blend-mode: soft-light;
    min-height: 100vh;

}
</style>