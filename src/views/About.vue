<template>
    <main>
        <Hero page="About Us"/>
        <Banner />
        <Categories />
        <Testimonial />
        <div class="container-fluid row row-cols-1 row-cols-md-3 row-cols-lg-4 g-4 text-center main-wrapper py-2">
            <div class="col" v-for="item in tags" :key="item.text">
                <div class="card h-100 border-0">
                    <div class="card-body">
                        <h5 class="card-title"><i class="color-main fs-2">{{ item.num }}</i></h5>
                        <h6 class="fs-6 text-black">{{ item.text }}</h6>
                    </div>
                </div>
            </div>

        </div>
    </main>
</template>

<script>
import Hero from '../components/Hero.vue';
import Banner from '../components/Banner.vue';
import Categories from '../components/Categories.vue';
import Testimonial from '../components/Testimonial.vue';

export default {
    components: { Hero, Banner, Categories, Testimonial },

    data() {
        return {
        tags: [
            {num: '3,000', text: 'OUR SATISFIED CUSTOMERS'},
            {num: '115', text: 'YEARS OF EXPERIENCE'},
            {num: '100', text: 'KINDS OF LIQUOR'},
            {num: '40', text: 'OUR BRANCHES'}
        ]
        }
    }
}
</script>
