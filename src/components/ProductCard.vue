<template>
  <div class="col">
    <div class="card border-0">
      <div
        class="card image-wrapper border-0"
        :style="{ background: 'url(' + `images/prod-${image}.jpg` + ')' }"
      >
        <!-- <img :src="`images/prod-${image}.jpg`" class="card-img" :alt="name"> -->
        <div
          class="card-img-overlay d-flex justify-content-center align-items-center"
        >
          <button
            type="button"
            class="btn btn-outline-light rounded-0 py-3 px-4 text-white bg-transparent card-btn"
          >
            <Icon icon="bi:handbag" />
          </button>
          <button
            type="button"
            class="btn btn-outline-light rounded-0 py-3 px-4 text-white bg-transparent card-btn mx-2"
          >
            <Icon icon="mdi:cards-heart-outline" />
          </button>
          <button
            type="button"
            class="btn btn-outline-light rounded-0 py-3 px-4 text-white bg-transparent card-btn"
          >
            <Icon icon="ic:outline-remove-red-eye" />
          </button>
        </div>
      </div>
      <div
        class="label py-0 px-2 text-white"
        :style="{ backgroundColor: labelBg }"
      >
        {{ label }}
      </div>
      <div class="card-body text-center">
        <p class="card-text mb-2">
          <i class="color-main">{{ kind }}</i>
        </p>
        <h5 class="card-title text-black">{{ name }}</h5>
        <p class="card-text">
          <i>{{ price }}</i>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import { Icon } from "@iconify/vue";

export default {
  components: { Icon },
  props: ["name", "label", "kind", "image", "price", "labelBg"],
};
</script>

<style scoped>
.image-wrapper {
  height: 330px;
  background-size: cover !important;
  background-repeat: no-repeat !important;
}

.card-img-overlay {
  background-color: rgba(0, 0, 0, 0.829);
  opacity: 0 !important;
  transition: opacity 1s ease;
}

.image-wrapper:hover .card-img-overlay {
  opacity: 1 !important;
}

.label {
  font-size: 0.7rem;
  background-color: #fff;
  width: fit-content;
}
</style>
