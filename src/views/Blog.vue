<template>
  <main>
    <Hero page="Blog" />
    <section class="main-wrapper container-fluid">
      <div class="row row-cols-1 row-cols-lg-2 g-4 mb-5">
        <PostCard v-for="post in blog" :key="post.image" :image="post.image" />
      </div>
      <nav aria-label="Page navigation mt-5">
        <ul class="pagination d-flex justify-content-center">
          <li class="page-item">
            <a
              class="page-link border-0 color-main"
              href="#"
              aria-label="Previous"
            >
              <span aria-hidden="true">&laquo;</span>
            </a>
          </li>
          <li class="page-item c-page-item">
            <a
              class="page-link active color-main rounded-circle d-flex align-items-center justify-content-center border-0"
              href="#"
              >1</a
            >
          </li>
          <li class="page-item c-page-item">
            <a
              class="page-link color-main rounded-circle d-flex align-items-center justify-content-center border-0"
              href="#"
              >2</a
            >
          </li>
          <li class="page-item c-page-item">
            <a
              class="page-link color-main rounded-circle d-flex align-items-center justify-content-center border-0"
              href="#"
              >3</a
            >
          </li>
          <li class="page-item c-page-item">
            <a
              class="page-link color-main rounded-circle d-flex align-items-center justify-content-center border-0"
              href="#"
              >4</a
            >
          </li>
          <li class="page-item c-page-item">
            <a
              class="page-link color-main rounded-circle d-flex align-items-center justify-content-center border-0"
              href="#"
              >5</a
            >
          </li>
          <li class="page-item">
            <a class="page-link border-0 color-main" href="#" aria-label="Next">
              <span aria-hidden="true">&raquo;</span>
            </a>
          </li>
        </ul>
      </nav>
    </section>
  </main>
</template>

<script>
import Hero from "../components/Hero.vue";
import PostCard from "../components/PostCard.vue";

export default {
  components: { Hero, PostCard },
  data() {
    return {
      blog: [
        { image: "1" },
        { image: "2" },
        { image: "3" },
        { image: "4" },
        { image: "5" },
        { image: "6" },
      ],
    };
  },
};
</script>

<style scoped>
.page-item .page-link {
  width: 44px;
  height: 44px;
}

.page-item .page-link:hover {
  color: var(--main-color);
  background: transparent;
}

.c-page-item .page-link.active {
  background-color: var(--main-color) !important;
  color: #fff;
}
</style>
