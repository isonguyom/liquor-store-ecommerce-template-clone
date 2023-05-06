
<template>
  <main>
    <!-- <section class="home-hero">
      <div class="hero-content">
        <h1><span class="outline-text">Good</span> Drink <span class="outline-text">for Good</span> Moments.</h1>
      </div>
    </section> -->
    <Hero :breadcrumb="false" height=110vh />
    <Banner />
    <Categories />
    <section class="container-fluid main-wrapper">
      <div class="card mb-5 border-0 bg-transparent">
        <p class="card-text text-center"><i class="color-main">Our Delightful offerings</i></p>
        <h2 class="card-title text-center text-black fw-bold">Tastefully Yours</h2>
      </div>
      <div class="row row-cols-1 row-cols-md-4 g-4">
        <ProductCard v-for="drink in drinks" :key="drink.name" :name="drink.name" :label="drink.label" :kind="drink.kind"
          :image="drink.image" :price="drink.price" :labelBg="drink.labelBg" />
      </div>
      <router-link class="bg-main text-decoration-none px-5 py-1 d-block mx-auto mt-5 text-center btn view-btn" :to="{ name: 'products' }">View All Products <Icon icon="ic:outline-arrow-right-alt" /></router-link>
    </section>
    <Testimonial />
    <section class="container-fluid main-wrapper">
      <div class="card mb-5 border-0 bg-transparent">
      <p class="card-text text-center"><i class="color-main">Blog</i></p>
      <h2 class="card-title text-center text-black fw-bold">Recent Blog</h2>
      </div>
      <div class="row row-cols-1 row-cols-lg-2 g-4">
       <PostCard  v-for="post in blog" :key="post.image" :image="post.image" />
      </div>
    </section>
  </main>
</template>

<script>
import { Icon } from '@iconify/vue';
import Hero from '../components/Hero.vue';
import Banner from '../components/Banner.vue';
import Categories from '../components/Categories.vue';
import Testimonial from '../components/Testimonial.vue';
import ProductCard from '../components/ProductCard.vue';
import PostCard from '../components/PostCard.vue';

export default {
  components: { Hero, Banner, Icon, Categories, Testimonial, ProductCard, PostCard },

  data() {
    return {
      drinks: [
        { name: 'Bacardi 151', kind: 'Brandy', image: '1', price: '69.00', label: 'Sale', labelBg: '#B7472A' },
        { name: 'Jim Beam Kentucky Straight', kind: 'Gin', image: '2', price: '69.00', label: 'Best Seller', labelBg: '#FE9801' },
        { name: 'Citadelle', kind: 'Rum', image: '3', price: '69.00', label: 'New Arrival', labelBg: '#01D28E' },
        { name: 'The Glenlivet', kind: 'Rum', image: '4', price: '69.00' },
        { name: 'Black Label', kind: 'Whiskey', image: '5', price: '69.00' },
        { name: 'Macallan', kind: 'Tequila', image: '6', price: '69.00' },
        { name: 'Old Monk', kind: 'Vodka', image: '7', price: '69.00' },
        { name: 'Jameson Irish Whiskey', kind: 'Whiskey', image: '8', price: '69.00' }
      ],
      blog: [
        { image: '1' },
        { image: '2' },
        { image: '3' },
        { image: '4' }
      ]
    }
  }
}
</script>

<style scoped>
.home-hero {
  background: url('/images/bg_2.jpg') fixed;
  background-size: cover;
  min-height: 100vh;
  background-color: black;
  color: #fff;
}

.hero-content {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%) rotate(-5deg);
  -ms-transform: translate(-50%, -50%) rotate(-5deg);
}

.outline-text {
  color: transparent;
  -webkit-text-stroke: 1px #fff;
}

.view-btn {
  width: 300px;
}

.view-btn:hover {
  background-color: var(--main-color);
  color: #fff;
}
</style>
