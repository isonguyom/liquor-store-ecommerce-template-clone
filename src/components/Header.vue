<template>
    <header class="Header position-absolute w-100">
        <div class="container-fluid top-nav main-wrapper py-2 py-md-1">
            <ul class="address nav d-flex align-itmes-center">
                <li class="me-2" v-for="item in address" :key="item.name"><a class="text-decoration-none text-white-50"
                        :href="`${item.name}:${item.value}`">
                        <Icon class="nav-icon me-1" :icon="item.icon" /> {{ item.value }}
                    </a>
                </li>
            </ul>
            <div class="multi-nav d-flex justify-content-between align-items-center mt-2 mt-md-0">
                <ul class="social-nav nav d-flex align-items-center">
                    <li class="me-2" v-for="item in social" :key="item.name"><a class="text-white" :href="item.link">
                            <Icon :icon="item.icon" />
                        </a></li>
                </ul>
                <ul class="account nav">
                    <li class="ms-3" v-for="item in account" :key="item.name"><a
                            class="text-decoration-none text-uppercase  text-white opacity-75" :href="item.link">{{
                                item.name }}</a></li>
                </ul>
            </div>
        </div>
        <!-- <nav class="main-nav">
            <a href=" " class="brand-name">
                Liquor <span>Store</span>
            </a>
            <div class="cart">
                <button class="orders-btn" @click="toggleCart">
                    <Icon icon="bi:handbag" /><span>3</span>
                </button>
                <div class="orders" :class="{ active: cartOpen }">
                    <router-link class="view-btn" to="{ name: 'cart' }">VIEW ALL</router-link>
                </div>
            </div>
            <button class="menu-toggler" @click="toggleMenu">Menu</button>
            <ul class="menu" :class="{ active: menuIsactive }">
                <li class="menu-item" :class="{ dropdownMenu: item.dropdown }" v-for="item in mainNav" :key="item.link">
                    <router-link class="menu-link" :to="{ name: item.name }" :disabled="!item.dropdown">{{ item.name }}
                        <Icon v-if="item.dropdown" icon="material-symbols:arrow-drop-down" />
                        <ul class="dropdown" v-if="item.dropdown">
                            <li class="dropdown-item" v-for="link in item.dropdownItems" :key="link.name"><router-link
                                    :to="{ name: link.link }">{{ link.name }}</router-link></li>
                        </ul>
                    </router-link>
                </li>
            </ul>

        </nav> -->
        <nav class="navbar navbar-expand-lg bg-black container-fluid main-wrapper py-3 main-nav" data-bs-theme="dark">
            <div class="d-flex flex-wrap justify-content-between align-items-center w-100">
                <a class="navbar-brand brand-name text-uppercase text-white fw-bold col-8 col-sm-4" href="#">Liquor <span
                        class="text-white-50">Store</span></a>
                <div class="cart">
                    <button type="button" class="btn bg-transparent color-main p-0 position-relative orders-btn"
                        @click="toggleCart">
                        <Icon icon="bi:handbag" /> <span
                            class="position-absolute top-0 start-100 d-flex justify-content-center align-itmes-center text-white-50 fw-light translate-middle badge rounded-circle bg-secondary">3</span>
                    </button>
                    <div class="orders position-absolute bg-white" :class="{ active: cartOpen }">
                        <router-link class="view-btn text-decoration-none" :to="{ name: 'cart' }">VIEW ALL</router-link>
                    </div>
                </div>
                <button @click="toggleMenu" class="navbar-toggler menu-toggler text-white-50 text-uppercase fs-6" type="button" data-bs-toggle="collapse"
                    data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false"
                    aria-label="Toggle navigation">
                    Menu
                </button>
                <div class="navbar-collapse" :class="{ collapse: menuIsActive }" id="navbarNavDropdown">
                    <ul class="navbar-nav menu">
                        <li class="nav-item menu-item text-uppercase" :class="{ dropdownMenu: item.dropdown }" v-for="item in mainNav"
                            :key="item.link">
                            <router-link class="menu-link nav-link" :to="{ name: item.name }" :disabled="!item.dropdown">{{
                                item.name }}
                                <Icon v-if="item.dropdown" icon="material-symbols:arrow-drop-down" />
                                <ul class="dropdown" v-if="item.dropdown">
                                    <li class="dropdown-item" v-for="link in item.dropdownItems" :key="link.name">
                                        <router-link class="text-decoration-none" :to="{ name: link.link }">{{ link.name }}</router-link>
                                    </li>
                                </ul>
                            </router-link>
                        </li>

                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>

<script>
import { Icon } from '@iconify/vue';

export default {
    components: {
        Icon,
    },

    data() {
        return {
            menuIsActive: true,
            cartOpen: false,
            address: [
                { name: 'tel', icon: 'solar:phone-bold', value: '+00 1234 567' },
                { name: 'email', icon: 'fa:send', value: 'youremail@email.com' },
            ],
            social: [
                { name: 'facebook', icon: 'uil:facebook-f', link: '#' },
                { name: 'twitter', icon: 'fe:twitter', link: '#' },
                { name: 'instagram', icon: 'ph:instagram-logo-bold', link: '#' },
                { name: 'web', icon: 'uil:basketball', link: '#' }
            ],
            account: [
                { name: 'Sign up', link: '' },
                { name: 'log in', link: '' }
            ],
            mainNav: [
                { name: 'home', link: 'home', dropdown: false },
                { name: 'about', link: 'about', dropdown: false },
                {
                    name: 'products', dropdown: true, dropdownItems: [
                        { name: 'products', link: 'products' },
                        { name: 'single product', link: 'single-product' },
                        { name: 'cart', link: 'cart' },
                        { name: 'checkout', link: 'checkout' },
                    ]
                },
                { name: 'blog', link: 'blog', dropdown: false },
                { name: 'contact', link: 'contact', dropdown: false }
            ]
        }
    },

    methods: {
        toggleMenu() {
            this.menuIsActive = !this.menuIsActive
        },

        toggleCart() {
            this.cartOpen = !this.cartOpen
        }
    }
}
</script>

<style scoped>
.Header {
    height: fit-content;
    z-index: 3;
}

.top-nav {
    background-color: #A23F25;
    height: fit-content;
    font-weight: 200;
}

ul.address {
    font-size: 0.8rem;
}


ul.social-nav {
    font-size: 0.85rem;
}

ul.social-nav a:hover {
    background-color: #b9472b;
}

ul.account {
    font-size: 0.8rem;
}

.cart {
    top: 1.4em;
    right: 8%;
    width: min-content;
}

.orders-btn {
    color: #A23F25;
}

.orders-btn:hover {
    color: #A23F25;
}

.orders-btn span {
    font-size: 0.8rem;
    width: 20px !important;
    height: 20px !important;
    background-color: rgba(128, 128, 128, 0.432) !important;
}

.orders {
  
    border-radius: 4px;
    width: 300px;
    right: -30px;
     display: none;
}

.orders.active {
    display: block;
}

.orders .view-btn {
    display: block;
    width: fit-content;
    margin-left: auto;
    margin-right: auto;
    text-align: center;
    color: #A23F25;
    font-size: 0.8rem;
    z-index: 2;
}

.main-nav .menu li {
    padding: 0.8em 0;
}

.main-nav .menu a {
    color: #fff;
    font-size: 0.9rem;
}

.menu .dropdown {
    background-color: #fff;
    text-transform: capitalize;
    border-radius: 3px;
    padding: 0.5em 1.2em;
    display: none;
}

.menu .dropdown li {
    padding: 0.5em;
}

.menu .dropdown a {
    color: #000000;
}

.menu li a:hover,
.menu li a.router-link-active,
.menu li a.router-link-exact-active {
    color: #A23F25;
}

.menu li .dropdown a:hover,
.menu li .dropdown a.router-link-active,
.menu li .dropdown a.router-link-exact-active {
    color: #000;
}

.main-nav .menu li.dropdownMenu:hover .dropdown {
    display: block;
}

@media (min-width: 344px) {
    .main-nav {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: space-between;
    }

    /* .cart {
        position: relative;
        top: auto;
        right: auto;
    } */

    .main-nav .menu {
        width: 100%;
    }
}

@media (min-width: 768px) {
    .top-nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    ul.address,
    .multi-nav {
        width: fit-content;
        margin-bottom: 0;
    }

    ul.social-nav {
        margin-right: 2em;
    }
}

@media (min-width: 992px) {
    .top-nav {
        padding: 0.3em 9%;
    }

    .main-nav {
        padding: 1em 9%;
    }

    .cart {
        position: absolute;
        right: 9%;
        margin-left: 2em;
    }

    .menu-toggler {
        display: none;
    }

    .main-nav .menu {
        width: fit-content;
        margin-right: 2em;
        display: block;
    }

    .main-nav .menu li {
        display: inline-block;
        position: relative;
        padding: 0.5em;
        margin: 0;
        text-align: center;
    }

    .main-nav .menu li a {
        color: gray;
    }

    .menu .dropdown {
        position: absolute;
        left: 0;
        height: max-content;
        width: max-content
    }

    .menu .dropdown li {
        display: block;
        text-align: left;
    }

    .menu li a.router-link-active,
    .menu li a.router-link-exact-active {
        color: #fff;
    }

    .menu li .dropdown a:hover,
    .menu li .dropdown a.router-link-active,
    .menu li .dropdown a.router-link-exact-active {
        color: #000;
    }
}

.main-nav.light {
    background-color: #fff;
}

.main-nav.light .brand-name {
    color: #000000;
}

.main-nav.light .brand-name span,
.main-nav.light .orders-btn span {
    color: #A23F25;
}

.main-nav.light .menu a {
    color: #000;
}

.main-nav.light .menu li a.router-link-active,
.main-nav.light .menu li a.router-link-exact-active {
    color: #A23F25;
}

.main-nav.light .menu li .dropdown a:hover,
.main-nav.light .menu li .dropdown a.router-link-active,
.main-nav.light .menu li .dropdown a.router-link-exact-active {
    color: #000;
}
</style>