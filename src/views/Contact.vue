<template>
  <main>
    <Hero page="Contact Us" />
    <section class="container-fluid main-wrapper">
      <div class="row">
        <div class="col-md-3 mb-3 mb-sm-0">
          <div class="card bg-transparent border-0">
            <div class="card-body">
              <div
                class="rounded-circle bg-main mx-auto mb-3 icon-wrapper text-center d-flex justify-content-center align-items-center">
                <Icon icon="fluent:location-48-filled" width="30" />
              </div>
              <p class="card-text text-center">
                <span class="text-black">Address: </span>198 West 21th Street,
                Suite 721 New York NY 10016
              </p>
            </div>
          </div>
        </div>
        <div class="col-md-3 mb-3 mb-sm-0">
          <div class="card bg-transparent border-0">
            <div class="card-body">
              <div
                class="rounded-circle bg-main mx-auto mb-3 icon-wrapper text-center d-flex justify-content-center align-items-center">
                <Icon icon="solar:phone-bold" width="30" />
              </div>
              <p class="card-text text-center">
                <span class="text-black">Phone: </span><a class="text-decoration-none color-main" href="tel:+1235235598">+
                  1235 2355 98</a>
              </p>
            </div>
          </div>
        </div>
        <div class="col-md-3 mb-3 mb-sm-0">
          <div class="card bg-transparent border-0">
            <div class="card-body">
              <div
                class="rounded-circle bg-main mx-auto mb-3 icon-wrapper text-center d-flex justify-content-center align-items-center">
                <Icon icon="fa:send" width="30" />
              </div>
              <p class="card-text text-center">
                <span class="text-black">Email: </span><a class="text-decoration-none color-main"
                  href="mailto:info@yoursite.com">
                  info@yoursite.com</a>
              </p>
            </div>
          </div>
        </div>
        <div class="col-md-3 mb-3 mb-sm-0">
          <div class="card bg-transparent border-0">
            <div class="card-body">
              <div
                class="rounded-circle bg-main mx-auto mb-3 icon-wrapper text-center d-flex justify-content-center align-items-center">
                <Icon icon="fa-solid:globe-asia" width="30" />
              </div>
              <p class="card-text text-center">
                <span class="text-black">Website: </span><a class="text-decoration-none color-main"
                  href="yoursite.com">yoursite.com</a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="container-fluid main-wrapper">
      <div class="row">
        <div class="col order-md-2">
          <form class="row g-3">
            <div class="col-md-6">
              <label for="inputEmail4" class="form-label text-uppercase color-main fs-6">Full Name</label>
              <input type="text" class="form-control form-control-lg border-0 border-bottom" id="inputEmail4"
                placeholder="Name" />
            </div>
            <div class="col-md-6">
              <label for="inputPassword4" class="form-label text-uppercase color-main fs-6">Email Address</label>
              <input type="email" class="form-control form-control-lg border-0 border-bottom" id="inputPassword4"
                placeholder="Email" />
            </div>
            <div class="col-12">
              <label for="inputAddress" class="form-label text-uppercase color-main fs-6">Subject</label>
              <input type="text" class="form-control form-control-lg border-0 border-bottom" id="inputAddress"
                placeholder="Subject" />
            </div>
            <div class="col-12">
              <label for="validationTextarea" class="form-label text-uppercase color-main fs-6">Message</label>
              <textarea class="form-control form-control-lg border-0 border-bottom" id="validationTextarea"
                placeholder="Message" required></textarea>
              <div class="invalid-feedback">
                Please enter a message in the textarea.
              </div>
            </div>
            <a class="btn bg-main py-2 px-4 btn-lg rounded-1 text-white" href="#" role="button">Send Message</a>
          </form>
        </div>
        <div class="col order-md-1">map</div>
      </div>
    </section>
  </main>
</template>

<script>
import { Icon } from "@iconify/vue";
import Hero from "../components/Hero.vue";

export default {
  components: { Hero, Icon },
};
</script>

<style scoped>
.icon-wrapper {
  width: 100px;
  height: 100px;
}

.btn {
  width: fit-content;
}

.btn:hover {
  background-color: var(--main-color);
}
</style>
