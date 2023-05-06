<template>
  <div class="col">
    <div class="card mb-3 border-0">
      <div class="row g-0">
        <div
          class="col-6 img-wrapper"
          :style="{ background: 'url(' + `images/image_${image}.jpg` + ')' }"
        ></div>
        <div class="col-6">
          <div class="card-body p-4 blog-text">
            <p class="card-text d-flex align-items-center">
              <Icon icon="fa:calendar" class="me-3" /> 23 April 2020
            </p>
            <i
              ><a href="" class="text-black text-decoration-none fs-5"
                >The Recipe from a Winemaker’s Restaurent</a
              ></i
            >
            <p class="card-text mt-3">
              A small river named Duden flows by their place and supplies it
              with the necessary regelialia.
            </p>
            <i
              ><a href="" class="fw-bold text-decoration-none color-main"
                >Continue <Icon icon="ic:outline-arrow-right-alt" /> </a
            ></i>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Icon } from "@iconify/vue";

export default {
  components: { Icon },
  props: ["image"],
};
</script>

<style scoped>
.img-wrapper {
  background-size: cover !important;
}

.blog-text a:hover {
  color: var(--main-color) !important;
}
</style>
