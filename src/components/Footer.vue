<template>
    <footer class="Footer">
        <div class="container-fluid main-wrapper">
            <div class="row row-cols-1 row-cols-md-3 row-cols-lg-5 g-4">
                <div class="col">
                    <div class="card bg-transparent border-0">
                        <div class="card-body px-0">
                            <h5 class="card-title mb-4"><a href=" "
                                    class="brand-name text-uppercase text-decoration-none text-white">
                                    Liquor <span class="text-white-50">Store</span>
                                </a></h5>
                            <p class="card-text text-white mb-4">Far far away, behind the word mountains, far from the
                                countries.</p>
                            <div>
                                <a class="social-link bg-main d-inline-flex align-items-center justify-content-center rounded-circle text-white-50"
                                    href="">
                                    <Icon icon="mdi:twitter" />
                                </a>
                                <a class="social-link bg-main d-inline-flex align-items-center justify-content-center rounded-circle text-white-50 mx-2"
                                    href="">
                                    <Icon icon="ri:facebook-fill" />
                                </a>
                                <a class="social-link bg-main d-inline-flex align-items-center justify-content-center rounded-circle text-white-50"
                                    href="">
                                    <Icon icon="ion:logo-instagram" />
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col" v-for="link in links" :key="link.title">
                    <div class="card bg-transparent border-0">
                        <div class="card-body px-0">
                            <h5 class="card-title text-white mb-4">{{ link.title }}</h5>
                            <ul class="nav flex-column px-0">
                                <li class="nav-item px-0" v-for="item, index in link.text" :key="index">
                                    <a class="nav-link p-0 mb-2 text-white-50" href="#">
                                        <Icon icon="ic:baseline-keyboard-arrow-right" />{{ item }}
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card bg-transparent border-0">
                        <div class="card-body px-0">
                            <h5 class="card-title text-white mb-4">Have a Questions?
                            </h5>
                            <p class="d-flex text-white mb-3">
                                <Icon class="nav-icon mr-4" icon="ion:map" width="45px" /> <span class="ms-3">203 Fake St.
                                    Mountain View, San Francisco, California, USA</span>
                            </p>
                            <a class="d-flex align-items-center text-decoration-none text-white-50 mb-3" href="">
                                <Icon class="nav-icon" icon="solar:phone-bold" /> <span class="d-block ms-3">+2 392
                                    3929 210</span>
                            </a>
                            <a class="d-flex align-items-center text-decoration-none text-white-50 mb-3" href="">
                                <Icon class="nav-icon" icon="fa:send" /> <span
                                    class="d-block ms-3">info@yourdomain.com</span>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="copyright container-fluid main-wrapper">
            Copyright ©2023 All rights reserved | This template is made with &#10084; by <span
                class="text-white">Colorlib.com</span>
        </div>
    </footer>
</template>

<script>
import { Icon } from '@iconify/vue';


export default {
    components: {
        Icon,
    },
    data() {
        return {
            links: [
                { title: 'My Account', text: ['My Account', 'Register', 'Log In', 'My Order'] },
                { title: 'Information', text: ['About us', 'Catalog', 'Contact us', 'Term & Conditions'] },
                { title: 'Quick Link', text: ['New User', 'Help Center', 'Report Spam', 'Faq\'s'] },
            ]
        }
    }
}
</script>

<style scoped>
.Footer {
    background-color: #1A1A1A;
}

.social-link {
    width: 44px;
    height: 44px;
}

.copyright {
    background-color: #000000;
}
</style>