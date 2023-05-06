<template>
  <main>
    <Hero page="Single Product" />
    <section class="container-fluid main-wrapper">
      <div class="row g-0 d-md-flex">
        <div class="col-lg-6 top-image">
          <a href="images/prod-1.jpg">
            <img class="w-100" src="/images/prod-1.jpg" alt="" />
          </a>
        </div>
        <div class="col-lg-6 mt-5 mt-lg-0">
          <div class="card-body px-3 px-lg-4 py-0">
            <h2 class="card-title text-black mb-3">Bacardi 151 Degree</h2>
            <small
              ><span class="color-main"
                >5.0
                <span>
                  <Icon icon="material-symbols:star-rounded" />
                  <Icon icon="material-symbols:star-rounded" />
                  <Icon icon="material-symbols:star-rounded" />
                  <Icon icon="material-symbols:star-rounded" />
                  <Icon icon="material-symbols:star-rounded" /> </span
              ></span>
              <span class="text-black ms-4"
                >100 <span class="text-black-50"> Rating </span></span
              >
              <span class="text-black ms-4"
                >500 <span class="text-black-50"> sold </span></span
              >
            </small>
            <h4 class="text-black mt-3 mb-4">$120.00</h4>
            <p class="card-text">
              A small river named Duden flows by their place and supplies it
              with the necessary regelialia. It is a paradisematic country, in
              which roasted parts of sentences fly into your mouth. <br /><br />
              On her way she met a copy. The copy warned the Little Blind Text,
              that where it came from it would have been rewritten a thousand
              times and everything that was left from its origin would be the
              word "and" and the Little Blind Text should turn around and return
              to its own, safe country.
            </p>
            <div class="input-group w-50 my-4">
              <span class="input-group-text bg-transparent rounded-0">-</span>
              <input
                type="text"
                class="form-control text-center mx-2"
                aria-label="Amount (to the nearest dollar)"
                value="1"
              />
              <span class="input-group-text bg-transparent rounded-0">+</span>
            </div>
            <p class="card-text">80 piece available</p>
            <a
              class="btn bg-main py-2 px-4 btn-lg rounded-1 text-white"
              href="#"
              role="button"
              >Add to Cart</a
            >
            <a
              class="btn bg-main py-2 px-5 btn-lg rounded-1 ms-3 text-white"
              href="#"
              role="button"
              >Buy now</a
            >
          </div>
        </div>
      </div>
    </section>
    <section class="container-fluid main-wrapper">
      <ul class="nav nav-pills mb-3">
        <li class="nav-item p-3 text-center border-0 c-tabs active">
          <a class="nav-link fw-bold text-black" aria-current="page" href="#"
            >Description</a
          >
        </li>
        <li class="nav-item p-3 text-center border-0 c-tabs mx-2">
          <a class="nav-link fw-bold text-black" href="#">Manufacturer</a>
        </li>
        <li class="nav-item p-3 text-center border-0 c-tabs">
          <a class="nav-link fw-bold text-black" href="#">Review</a>
        </li>
      </ul>
      <div id="" class="card-body c-bg p-4">
        <h5 class="card-title mb-4 text-black">Bacardi 151 Degree</h5>
        <p class="card-text">
          On her way she met a copy. The copy warned the Little Blind Text, that
          where it came from it would have been rewritten a thousand times and
          everything that was left from its origin would be the word "and" and
          the Little Blind Text should turn around and return to its own, safe
          country. But nothing the copy said could convince her and so it didn’t
          take long until a few insidious Copy Writers ambushed her, made her
          drunk with Longe and Parole and dragged her into their agency, where
          they abused her for their.
        </p>
      </div>
      <div class="card-body c-bg p-4">
        <h5 class="card-title mb-4 text-black">Manufactured By Liquor Store</h5>
        <p class="card-text">
          On her way she met a copy. The copy warned the Little Blind Text, that
          where it came from it would have been rewritten a thousand times and
          everything that was left from its origin would be the word "and" and
          the Little Blind Text should turn around and return to its own, safe
          country. But nothing the copy said could convince her and so it didn’t
          take long until a few insidious Copy Writers ambushed her, made her
          drunk with Longe and Parole and dragged her into their agency, where
          they abused her for their.
        </p>
      </div>
      <div class="card-body c-bg p-4 row">
        <div class="col-md-8">
          <h4 class="card-title text-black mb-4">23 Reviews</h4>
          <div class="col">
            <div
              class="card mb-3 bg-transparent border-0"
              v-for="id in clients"
              :key="id.id"
            >
              <div class="d-flex">
                <div class="potrait rounded-circle">
                  <img
                    :src="`images/person_${id.id}.jpg`"
                    class="d-block rounded-circle"
                    :alt="`person ${id.id}`"
                  />
                </div>
                <div>
                  <div class="card-body ps-3">
                    <div
                      class="d-flex justify-content-between align-items-center"
                    >
                      <h6 class="card-title text-black">Jacob Webb</h6>
                      <span class="text-body-secondary">25 April 2020</span>
                    </div>
                    <div class="color-main my-3">
                      <Icon icon="material-symbols:star-rounded" />
                      <Icon icon="material-symbols:star-rounded" />
                      <Icon icon="material-symbols:star-rounded" />
                      <Icon icon="material-symbols:star-rounded" />
                      <Icon icon="material-symbols:star-rounded" />
                    </div>
                    <p class="card-text">
                      When she reached the first hills of the Italic Mountains,
                      she had a last view back on the skyline of her hometown
                      Bookmarksgrov
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-4 px-3 mt-3 mt-md-0">
          <h4 class="card-title text-black mb-4">Give a Review</h4>
          <div>
            <div class="d-flex justify-content-between align-items-center">
              <div class="color-main d-flex align-items-center">
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <span class="text-black-50">(98%)</span>
              </div>
              <p>20 Reviews</p>
            </div>
            <div class="d-flex justify-content-between align-items-center">
              <div class="color-main d-flex align-items-center">
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <span class="text-black-50">(85%)</span>
              </div>
              <p>10 Reviews</p>
            </div>
            <div class="d-flex justify-content-between align-items-center">
              <div class="color-main d-flex align-items-center">
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <span class="text-black-50">(98%)</span>
              </div>
              <p>5 Reviews</p>
            </div>
            <div class="d-flex justify-content-between align-items-center">
              <div class="color-main d-flex align-items-center">
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <span class="text-black-50">(98%)</span>
              </div>
              <p>0 Reviews</p>
            </div>
            <div class="d-flex justify-content-between align-items-center">
              <div class="color-main d-flex align-items-center">
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <Icon icon="material-symbols:star-rounded" />
                <span class="text-black-50">(98%)</span>
              </div>
              <p>0 Reviews</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import { Icon } from "@iconify/vue";

import Hero from "../components/Hero.vue";
export default {
  components: { Hero, Icon },
  data() {
    return {
      clients: [{ id: "1" }, { id: "2" }, { id: "3" }],
    };
  },
};
</script>

<style scoped>
.btn:hover {
  background-color: var(--main-color);
}

.top-image img {
  max-height: 600px;
}

.c-tabs,
.c-bg {
  background-color: #f2f2f2;
}

.c-tabs:hover,
.c-tabs.active {
  background-color: var(--main-color);
  color: #fff;
}

.c-tabs:hover a,
.c-tabs.active a {
  color: #fff !important;
}

.potrait img {
  width: 100px;
  height: 100px;
}
</style>
