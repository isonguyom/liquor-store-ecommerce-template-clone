<template>
    <section class="Banner container-fluid main-wrapper py-0 text-white">
        <div class="row row-cols-1 row-cols-md-3">
            <div class="col p-4 py-5 py-lg-5 px-lg-3 mx-auto d-lg-flex align-items-lg-start justify-between"
                v-for="item in banner" :key="item.title" :style="{ backgroundColor: item.bgColor }">
                <img :src="`images/banner_${item.icon}.png`" class="card-img-top d-block banner-icon mt-lg-4"
                    :alt="item.title">
                <div class="card-body px-0 mt-3 ms-lg-4">
                    <h6 class="card-title mb-2">{{ item.title }}</h6>
                    <p class="card-text opacity-75">{{ item.text }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import { Icon } from '@iconify/vue';

export default {
    components: {
        Icon,
    },

    data() {
        return {
            banner: [
                {
                    icon: '1',
                    title: 'ONLINE SUPPORT 24/7',
                    text: 'A small river named Duden flows by their place and supplies it with the necessary regelialia.',
                    bgColor: 'transparent'
                },
                {
                    icon: '2',
                    title: 'MONEY BACK GUARANTEE',
                    text: 'A small river named Duden flows by their place and supplies it with the necessary regelialia.',
                    bgColor: '#AB4227'
                },
                {
                    icon: '3',
                    title: 'FREE SHIPPING & RETURN',
                    text: 'A small river named Duden flows by their place and supplies it with the necessary regelialia.',
                    bgColor: '#A23F25'
                },
            ]
        }
    }
}
</script>

<style scoped>
.Banner {
    background-color: #B7472A;
}

.col {
    max-width: 500px;
}

.banner-icon {
    width: 60px;

}
</style>