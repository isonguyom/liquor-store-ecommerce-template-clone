<template>
  <main>
    <Hero page="My cart" />
    <section class="container-fluid main-wrapper">
      <div class="table-responsive">
        <table class="table product-table">
          <thead class="bg-main py-4">
            <tr>
              <th scope="col"></th>
              <th scope="col"></th>
              <th scope="col py-4">Product</th>
              <th scope="col">Price</th>
              <th scope="col">Quantity</th>
              <th scope="col">total</th>
              <th scope="col"></th>
            </tr>
          </thead>
          <tbody class="text-black-50">
            <tr v-for="item in orders" :key="item.id">
              <th class="align-middle" scope="row">
                <input
                  class="border border-light-subtle"
                  type="checkbox"
                  name=""
                  id=""
                />
              </th>
              <td class="align-middle">
                <img
                  :src="`images/prod-${item.id}.jpg`"
                  class="img-fluid d-block side-img"
                  :alt="`product ${item.id}.jpg`"
                />
              </td>
              <td class="align-middle">
                <div class="card mb-3 bg-transparent border-0">
                  <div class="card-body">
                    <h5 class="card-title text-black">
                      Jim Beam Kentucky Straight
                    </h5>
                    <p class="card-text opacity-75">
                      Fugiat voluptates quasi nemo, ipsa perferendis
                    </p>
                  </div>
                </div>
              </td>
              <td class="align-middle">{{ item.price }}</td>
              <td class="align-middle">
                <input
                  class="w-50 p-3 border border-light-subtle"
                  type="number"
                  :name="`product ${item.id}.jpg`"
                  :id="`product ${item.id}.jpg`"
                  :value="item.qty"
                />
              </td>
              <td class="align-middle">{{ item.price * item.qty }}</td>
              <td class="align-middle">
                <button class="btn border-0 color-main">x</button>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </section>
    <section
      class="container-fluid main-wrapper d-md-flex justify-content-md-end"
    >
      <div class="card border-0 bg-transparent col-md-6 col-lg-4">
        <h4 class="card-title text-black">Cart Totals</h4>
        <div>
          <table class="table table-borderless mb-4">
            <tbody>
              <tr>
                <td>Subtotal</td>
                <td>$20.60</td>
              </tr>
              <tr>
                <td>Delivery</td>
                <td>$0.00</td>
              </tr>
              <tr>
                <td>Discount</td>
                <td>$3.00</td>
              </tr>
            </tbody>
            <tfoot class="mt-4 border-top">
              <tr>
                <td>TOTAL</td>
                <th>$17.60</th>
              </tr>
            </tfoot>
          </table>
          <router-link
            :to="{ name: 'checkout' }"
            class="btn bg-main w-100 py-2 px-4 btn-lg rounded-1 text-white"
            href="#"
            role="button"
            >Proceed to Checkout</router-link
          >
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import Hero from "../components/Hero.vue";

export default {
  components: { Hero },
  data() {
    return {
      orders: [
        { id: 1, image: "", price: 44.99, qty: 2 },
        { id: 2, image: "", price: 30.99, qty: 1 },
        { id: 3, image: "", price: 35.5, qty: 1 },
        { id: 4, image: "", price: 76.99, qty: 1 },
        { id: 5, image: "", price: 40.99, qty: 3 },
      ],
    };
  },
};
</script>

<style scoped>
.product-table thead th {
  padding: 30px 10px;
}

.product-table tbody th,
.product-table tbody td {
  padding: 0 10px;
}

.side-img {
  width: 60px;
  height: 70px;
}

.btn.color-main:hover {
  background-color: transparent;
  color: var(--main-color);
}

.btn:hover {
  background-color: var(--main-color);
}
</style>
