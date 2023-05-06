<template>
  <section
    class="Hero container-fluid main-wrapper"
    :style="{ height: height }"
  >
    <div
      class="hero-content text-center position-absolute top-50 start-50"
      v-if="breadcrumb"
    >
      <div class="text-uppercase fs-6">
        <span>home <Icon icon="ic:baseline-keyboard-arrow-right" /></span>
        <span class="ms-3"
          >{{ page }} <Icon icon="ic:baseline-keyboard-arrow-right"
        /></span>
      </div>
      <h1 class="text-white text-center">{{ page }}</h1>
    </div>
    <div
      class="hero-content hero-content-home position-absolute top-50 start-50 col-12 col-sm-8 text-center text-white fw-bold"
      v-else
    >
      <i class="fw-bold lh-1"
        ><span class="outline-text">Good</span> Drink
        <span class="outline-text">for Good</span> Moments<span
          class="outline-text"
          >.</span
        ></i
      >
      <div class="mt-5">
        <button type="button" class="btn bg-main me-2 px-4">Shop Now</button>
        <button type="button" class="btn btn-outline-light px-4">
          Read More
        </button>
      </div>
    </div>
  </section>
</template>

<script>
import { Icon } from "@iconify/vue";

export default {
  components: { Icon },
  props: {
    breadcrumb: {
      default: true,
    },
    height: {
      default: "70vh",
    },
    page: {
      type: String,
    },
  },
};
</script>
<style scoped>
.Hero {
  height: 100vh;
  background: url("/images/bg_2.jpg") fixed;
  background-size: cover;
  background-color: rgba(0, 0, 0, 0.295);
  background-blend-mode: soft-light;
  min-height: 50vh;
}

.hero-content {
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
}

.hero-content-home {
  transform: translate(-50%, -50%) rotate(-5deg);
  -ms-transform: translate(-50%, -50%) rotate(-5deg);
}

.hero-content-home i,
.hero-content h1 {
  font-size: 2.5rem !important;
}

.hero-content-home button:hover {
  background-color: var(--main-color);
  color: #fff;
  border: 1px solid var(--main-color);
}

.outline-text {
  color: transparent;
  -webkit-text-stroke: 1px #ffffffe5;
}

@media screen and (min-width: 576px) {
  .hero-content-home i,
  .hero-content h1 {
    font-size: 4.5rem !important;
  }
}
</style>
