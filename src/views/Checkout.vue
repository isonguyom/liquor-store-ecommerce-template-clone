<template>
  <main>
    <Hero page="Checkout" />
    <section class="main-wrapper container-fluid">
      <h4 class="card-title text-black">Billing Details</h4>
      <form class="row g-3 needs-validation mt-4" novalidate>
        <div class="col-md-6">
          <label for="validationCustom01" class="form-label text-black"
            >First Name</label
          >
          <input
            type="text"
            class="form-control form-control-lg"
            id="validationCustom01"
            required
          />
          <div class="valid-feedback">Looks good!</div>
        </div>
        <div class="col-md-6">
          <label for="validationCustom02" class="form-label text-black"
            >Last Name</label
          >
          <input
            type="text"
            class="form-control form-control-lg"
            id="validationCustom02"
            required
          />
          <div class="valid-feedback">Looks good!</div>
        </div>
        <div class="col-12">
          <label for="validationCustom04" class="form-label text-black"
            >State/Country</label
          >
          <select
            class="form-select form-control-lg"
            id="validationCustom04"
            required
            placeholder="France"
          >
            <option selected value="france">France</option>
            <option value="nigeria">Nigeria</option>
            <option value="ghana">Ghana</option>
            <option value="niger">Niger</option>
          </select>
          <div class="invalid-feedback">Please select a valid state.</div>
        </div>
        <div class="col-12">
          <label class="form-label text-black">Street Address</label>
          <div class="row g-3">
            <div class="col-md-6">
              <input
                type="text"
                class="form-control form-control-lg"
                id="validationCustom03"
                required
                placeholder="House number and street name"
              />
              <div class="invalid-feedback">Please provide a valid house number and street name.</div>
            </div>
            <div class="col-md-6">
              <input
                type="text"
                class="form-control form-control-lg"
                id="validationCustom04"
                required
                placeholder="Apartment, suite, unit etc: (optional)"
              />
              <div class="invalid-feedback">Please provide a valid Apartment.</div>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <label class="form-label text-black">Town / City</label>
          <input
            type="text"
            class="form-control form-control-lg"
            id="validationCustom05"
            required
          />
          <div class="invalid-feedback">Please provide a valid city.</div>
        </div>
        <div class="col-md-6">
          <label for="validationCustom05" class="form-label text-black"
            >Postcode/ZIP*</label
          >
          <input
            type="text"
            class="form-control form-control-lg"
            id="validationCustom06"
            required
          />
          <div class="invalid-feedback">Please provide a valid zip.</div>
        </div>
        <div class="col-md-6">
          <label for="exampleFormControlInput1" class="form-label text-black"
            >Phone</label
          >
          <input
            type="tel"
            class="form-control form-control-lg"
            id="exampleFormControlInput1"
          />
          <div class="invalid-feedback">Please provide a valid Phone number.</div>
        </div>
        <div class="col-md-6">
          <label for="exampleFormControlInput1" class="form-label text-black"
            >Email Address</label
          >
          <input
            type="email"
            class="form-control form-control-lg"
            id="exampleFormControlInput2"
          />
          <div class="invalid-feedback">Please provide a valid email.</div>
        </div>
        <div class="col-12 d-flex">
          <div class="form-check me-4">
            <input
              class="form-check-input"
              type="radio"
              name="flexRadioDefault"
              id="flexRadioDefault1"
            />
            <label class="form-check-label" for="flexRadioDefault1">
              Create an Account?
            </label>
          </div>
          <div class="form-check">
            <input
              class="form-check-input"
              type="radio"
              name="flexRadioDefault"
              id="flexRadioDefault2"
              checked
            />
            <label class="form-check-label" for="flexRadioDefault2">
              Ship to different address
            </label>
          </div>
        </div>
      </form>
    </section>

    <section class="main-wrapper container-fluid row g-4">
      <div class="card border-0 bg-transparent col-md-6 mb-3 mb-md-0 px-4">
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
        </div>
      </div>
      <div class="card border-0 bg-transparent col-md-6 px-4">
        <h4 class="card-title text-black">Payment Method</h4>
        <div class="form-check mb-3">
          <input
            class="form-check-input"
            type="radio"
            name="flexRadioDefault"
            id="flexRadioDefault1"
          />
          <label class="form-check-label" for="flexRadioDefault1">
            Direct Bank Tranfer
          </label>
        </div>
        <div class="form-check mb-3">
          <input
            class="form-check-input"
            type="radio"
            name="flexRadioDefault"
            id="flexRadioDefault2"
            checked
          />
          <label class="form-check-label" for="flexRadioDefault2">
            Check Payment
          </label>
        </div>
        <div class="form-check mb-3">
          <input
            class="form-check-input"
            type="radio"
            name="flexRadioDefault"
            id="flexRadioDefault3"
            checked
          />
          <label class="form-check-label" for="flexRadioDefault3">
            Paypal
          </label>
        </div>
        <div class="form-check mb-3">
          <input
            class="form-check-input"
            type="checkbox"
            value=""
            id="flexCheckDefault"
          />
          <label class="form-check-label" for="flexCheckDefault">
            I have read and accept the terms and conditions
          </label>
        </div>
        <a
          class="btn bg-main w-100 py-2 px-4 btn-lg rounded-1 text-white"
          href="#"
          role="button"
          >Place an order</a
        >
      </div>
    </section>
  </main>
</template>

<script>
import Hero from "../components/Hero.vue";

export default {
  components: { Hero },
};
</script>

<style scoped>
.btn:hover {
  background-color: var(--main-color);
}

input, select {
  font-size: 0.7rem;
  opacity: 0.6;
}
</style>
