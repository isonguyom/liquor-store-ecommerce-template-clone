<template>
  <div
    class="card col mb-3 p-4 bg-transparent text-white border border-opacity-75"
  >
    <div
      class="quote-icon rounded-circle position-absolute d-flex align-items-center justify-content-center"
    >
      <Icon icon="bxs:quote-left" />
    </div>
    <i class="opacity-75"
      >When she reached the first hills of the Italic Mountains, she had a last
      view back on the skyline of her hometown Bookmarksgrov</i
    >
    <div class="d-flex align-items-center">
      <div>
        <img
          :src="`images/person_${image}.jpg`"
          class="img-fluid rounded-circle potrait"
          alt="..."
        />
      </div>
      <div>
        <div class="card-body">
          <h5 class="card-title">Roger Scott</h5>
          <p class="card-text opacity-75">Marketing Manager</p>
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
.quote-icon {
  width: 40px;
  height: 40px;
  background-color: var(--main-color);
  top: -20px;
}

.potrait {
  width: 70px;
  height: 70px;
}
</style>
