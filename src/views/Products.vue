<template>
  <main>
    <Hero page="Products" />
    <section class="container-fluid main-wrapper">
      <div class="row">
        <div class="col-md-8">
          <div class="d-flex justify-content-between mb-4">
            <p class="card-title text-black">Select Types of Products</p>
            <select
              class="form-select c-select border-0"
              size="1"
              aria-label="size 1 select example"
            >
              <option class="text-black-50" selected disabled>
                Nothing selected
              </option>
              <option v-for="type in drinkType" :key="type.id" :value="type.id">
                {{ type.type }}
              </option>
            </select>
          </div>
          <div class="row row-cols-1 row-cols-md-3 g-4">
            <ProductCard
              v-for="drink in drinks"
              :key="drink.name"
              :name="drink.name"
              :label="drink.label"
              :kind="drink.kind"
              :image="drink.image"
              :price="drink.price"
              :labelBg="drink.labelBg"
            />
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
                <a
                  class="page-link border-0 color-main"
                  href="#"
                  aria-label="Next"
                >
                  <span aria-hidden="true">&raquo;</span>
                </a>
              </li>
            </ul>
          </nav>
        </div>
        <div class="col-md-4">
          <div class="card border-0 p-0">
            <div class="card-body px-0 pt-0">
              <h5 class="card-title text-black">Product Types</h5>
            </div>
            <ul class="list-group list-group-flush">
              <li
                class="list-group-item px-0"
                v-for="type in drinkType"
                :key="type.id"
              >
                <a
                  href="#"
                  class="card-link text-decoration-none text-black d-flex justify-content-between flex-nowrap"
                  >{{ type.type
                  }}<Icon
                    class="text-black-50"
                    icon="ic:baseline-keyboard-arrow-right"
                /></a>
              </li>
            </ul>
          </div>
          <div class="card border-0 mt-5">
            <div class="card-body px-0">
              <h5 class="card-title text-black">Recent Blog</h5>
            </div>
            <div
              class="card mb-4 border-0"
              v-for="(image, index) in blog"
              :key="index"
            >
              <div class="row g-0">
                <div class="col-4">
                  <img
                    :src="`images/image_${image}.jpg`"
                    class="img-fluid rounded-start"
                    alt="..."
                  />
                </div>
                <div class="col-8">
                  <div class="card-body py-0">
                    <p class="card-text">
                      <a class="text-decoration-none text-black" href="">
                        Even the all-powerful Pointing has no control about the
                        blind texts
                      </a>
                    </p>
                    <div class="card-body p-0">
                      <small
                        ><a
                          href="#"
                          class="card-link text-black-50 text-decoration-none"
                          ><Icon icon="fa:calendar" /> Apr. 18, 2020</a
                        ></small
                      >
                      <small class="ms-3"
                        ><a
                          href="#"
                          class="card-link text-black-50 text-decoration-none"
                          ><Icon icon="fa6-solid:comment" /> 19</a
                        ></small
                      >
                    </div>
                  </div>
                </div>
              </div>
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
import ProductCard from "../components/ProductCard.vue";

export default {
  components: { Icon, Hero, ProductCard },

  data() {
    return {
      drinks: [
        {
          name: "Bacardi 151",
          kind: "Brandy",
          image: "1",
          price: "69.00",
          label: "Sale",
          labelBg: "#B7472A",
        },
        {
          name: "Jim Beam Kentucky Straight",
          kind: "Gin",
          image: "2",
          price: "69.00",
          label: "Best Seller",
          labelBg: "#FE9801",
        },
        {
          name: "Citadelle",
          kind: "Rum",
          image: "3",
          price: "69.00",
          label: "New Arrival",
          labelBg: "#01D28E",
        },
        { name: "The Glenlivet", kind: "Rum", image: "4", price: "69.00" },
        { name: "Black Label", kind: "Whiskey", image: "5", price: "69.00" },
        { name: "Macallan", kind: "Tequila", image: "6", price: "69.00" },
        { name: "Old Monk", kind: "Vodka", image: "7", price: "69.00" },
        {
          name: "Jameson Irish Whiskey",
          kind: "Whiskey",
          image: "8",
          price: "69.00",
        },
        { name: "Screwball", kind: "Whiskey", image: "9", price: "69.00" },
        { name: "Jack Daniel's", kind: "Whiskey", image: "10", price: "69.00" },
        { name: "McClelland's", kind: "Whiskey", image: "11", price: "69.00" },
        { name: "Plantation", kind: "Whiskey", image: "12", price: "69.00" },
      ],
      drinkType: [
        { type: "Brandy", id: "1" },
        { type: "Gin", id: "2" },
        { type: "Rum", id: "3" },
        { type: "Tequila", id: "4" },
        { type: "Vodka", id: "5" },
        { type: "Whiskey", id: "6" },
      ],
      blog: ["1", "2", "3"],
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

.c-select {
  width: fit-content;
}
</style>
