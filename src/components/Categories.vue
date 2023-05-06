<template>
  <section class="container-fluid main-wrapper">
    <div class="row g-0 d-md-flex align-items-center">
      <div class="col-md-6 top-image"></div>
      <div class="col-md-6">
        <div class="card-body px-3 px-lg-4 py-5">
          <i class="color-main"><small>Since 1905</small></i>
          <h2 class="card-title text-black fw-bold mb-4">
            Desire Meets A New Taste
          </h2>
          <p class="card-text">
            A small river named Duden flows by their place and supplies it with
            the necessary regelialia. It is a paradisematic country, in which
            roasted parts of sentences fly into your mouth. <br /><br />
            On her way she met a copy. The copy warned the Little Blind Text,
            that where it came from it would have been rewritten a thousand
            times and everything that was left from its origin would be the word
            "and" and the Little Blind Text should turn around and return to its
            own, safe country.
          </p>
          <p class="card-text fs-3 text-black">
            <i class="color-main">115</i> Years of Experience In Business
          </p>
        </div>
      </div>
    </div>
    <div class="row row-cols-1 row-cols-md-3 row-cols-lg-6 g-4 mt-5">
      <div class="col" v-for="type in wineType" :key="type.type">
        <div class="card border-0">
          <div
            class="kind-wrapper rounded-circle d-flex align-items-center justify-content-center mx-auto"
          >
            <img
              :src="`images/kind-${type.image}.jpg`"
              class="card-img-top rounded-circle d-block"
              :alt="type.type"
            />
            <div class="c-overlay rounded-circle"></div>
          </div>
          <div class="card-body text-center mx-auto">
            <h5 class="card-title text-black">{{ type.type }}</h5>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      wineType: [
        { type: "Brandy", image: "1" },
        { type: "Gin", image: "2" },
        { type: "Rum", image: "3" },
        { type: "Tequila", image: "4" },
        { type: "Vodka", image: "5" },
        { type: "Whiskey", image: "6" },
      ],
    };
  },
};
</script>

<style scoped>
.top-image {
  background: url("/images/about.jpg");
  height: 420px;
  background-size: cover;
}

.kind-wrapper {
  border: 1px solid var(--main-color);
  height: 140px;
  width: 140px;
  transition: border 0.7s ease;
}

.kind-wrapper img {
  height: 120px;
  width: 120px;
}

.c-overlay {
  width: 100px;
  height: 100px;
  background-color: #ffffff81;
  position: absolute;
  transition: all 1s ease;
  opacity: 0;
}

.kind-wrapper:hover {
  border: none;
}

.kind-wrapper:hover .c-overlay {
  opacity: 1;
}

.main-wrapper {
  padding: 60px 0 !important;
}

@media screen and (min-width: 768px) {
  .top-image {
    height: 650px !important;
  }

  .main-wrapper {
    padding: 60px 8% !important;
  }
}

@media screen and (min-width: 992px) {
  .top-image {
    height: 420px !important;
  }
}
</style>
