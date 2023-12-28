<template>
    <!-- <footer class="py-5">
        <div class="container">
            <div class="footer-cont d-flex justify-content-between gap-5">
                <div class="logo">
                    <router-link class="text-decoration-none" :to="`/${$i18n.locale}`">
                        <img :src="`https://seasonreal.seasonsge.com/${info.logo}`" alt="">
                    </router-link>
                </div>
                <ul class="links d-flex gap-5">
                    <div class="d-flex flex-column gap-4">
                        <li>
                            <router-link class="text-decoration-none fw-bold text-white fs-5"
                                :to="`/${$i18n.locale}`">{{ $t('footerLinks[0]') }}</router-link>
                        </li>
                        <li>
                            <a v-if="router.currentRoute.value.path === `/${$route.params.lang}`"
                                class="text-decoration-none fw-bold text-white fs-5" href="#about">{{ $t('footerLinks[1]') }}</a>
                            <router-link v-else class="text-decoration-none fw-bold text-white fs-5"
                                :to="`/${$i18n.locale}`">{{ $t('footerLinks[1]') }}</router-link>
                        </li>
                    </div>
                    <div class="d-flex flex-column gap-4">
                        <li>
                            <router-link class="text-decoration-none fw-bold text-white fs-5"
                                :to="`/${$i18n.locale}/programmes`">{{ $t('footerLinks[2]') }}</router-link>
                        </li>
                        <li>
                            <router-link class="text-decoration-none fw-bold text-white fs-5"
                                :to="`/${$i18n.locale}/contact`">{{ $t('footerLinks[3]') }}</router-link>
                        </li>
                    </div>
                    <div class="d-flex flex-column gap-4">
                        <li>
                            <router-link class="text-decoration-none fw-bold text-white fs-5"
                                :to="`/${$i18n.locale}/privacy-policy`">
                                {{ $t('footerLinks[4]') }}
                            </router-link>
                        </li>
                        <li>
                            <router-link class="text-decoration-none fw-bold text-white fs-5"
                                :to="`/${$i18n.locale}/terms-and-conditions`">
                                {{ $t('footerLinks[5]') }}
                            </router-link>
                        </li>
                    </div>
                </ul>
                <div class="contacts-info d-flex flex-column gap-3">
                    <a class="d-flex gap-3 text-white-50" :href="info.longitude" target="_blank">
                        <i class="fa-solid fa-location-dot text-white"></i>
                        {{ $i18n.locale === 'en' ? info.english_title : info.arabic_title }}
                    </a>
                    <a class="d-flex gap-3 text-white-50" target="_blank" :href="`tel:${info.mobile_number}`">
                        <i class="fa-solid fa-phone text-white"></i>
                        {{ info.mobile_number }}
                    </a>
                    <a class="d-flex gap-3 text-white-50" :href="`mailto:${info.email}`">
                        <i class="fa-solid fa-envelope text-white"></i>
                        {{ info.email }}
                    </a>
                </div>
            </div>
            <span class="copyright mt-5 d-block text-end text-white">
                &copy; Copyright {{ new Date(Date.now()).getFullYear() }} Seasons Tour, All right reserved
                <router-link :to="`/${$i18n.locale}/privacy-policy`">
                    {{ $t('footerLinks[4]') }}
                </router-link> &
                <router-link :to="`/${$i18n.locale}/terms-and-conditions`">
                    {{ $t('footerLinks[5]') }}
                </router-link></span>
        </div>
    </footer> -->
    <footer>
        <section class="col-10 mx-auto my-3">
            <div class="d-flex flex-wrap align-items-center justify-content-lg-between justify-center">
                <div class="col-3 mt-lg-0 my-2"><img src="../assets/Images/sky-logo.png" class="footer-image" alt=""></div>
                    <div class="d-flex col-lg gap-3 justify-content-between w-100">
                        <div class="d-flex justify-content-center align-items-center text-white bg-success social-link"><i class="fa-brands fa-whatsapp fs-4"></i></div>
                        <div class="d-flex justify-content-center align-items-center text-white bg-red social-link"><i class="fa-brands fa-instagram fs-4"></i></div>
                        <div class="d-flex justify-content-center align-items-center text-white bg-blue social-link"><i class="fa-brands fa-twitter fs-4"></i></div>
                        <div class="d-flex justify-content-center align-items-center text-white bg-primary social-link"><i class="fa-brands fa-facebook-f fs-4"></i></div>
                        <div class="d-flex justify-content-center align-items-center text-white bg-warning social-link"><i class="fa-brands fa-snapchat fs-4"></i></div>
                        <div class="d-flex justify-content-center align-items-center text-white bg-black social-link"><i class="fa-brands fa-tiktok fs-4"></i></div>
                        <div class="d-flex justify-content-center align-items-center text-white bg-danger social-link"><i class="fa-brands fa-youtube fs-4"></i></div>
                    </div>
            </div>
        </section>
        <section class="d-flex flex-wrap col-10 mx-auto my-5">
            <div class="col-md-6">
                <h3 class="text-3xl font-semibold main-color">{{ $t('footer.address.tit') }}</h3>
                <h5 class="fw-semibold my-2 mt-4">{{ $t('footer.address.details') }}</h5>
                <h5 class="fw-semibold my-2">{{ $t('footer.address.tel') }}</h5>
                <h5 class="fw-semibold my-2">{{ $t('footer.address.email') }}</h5>
            </div>
            <div class="col-md-6">
                <h3 class="text-3xl font-semibold main-color">{{ $t('footer.linksTit') }}</h3>
                <ul class="mt-4">
                    <template v-for="item,index in $tm('footer.links')" :key="index">
                        <li class="fs-5 fw-semibold my-3">{{ item }}</li>
                    </template>
                </ul>
            </div>
        </section>
        <section class="bg-main-color py-2 text-center">
            <p class="fs-5 fw-semibold text-white">{{ $t('footer.para') }}</p>
        </section>
    </footer>
</template>
<script setup>
import { useRouter } from 'vue-router'
import { ref, onMounted } from 'vue'
import axios from 'axios'

const router = useRouter()
const info = ref([])

onMounted(async () => {
    await axios.get("https://seasonreal.seasonsge.com/appv1real/info")
        .then(data => {
            info.value = data.data[0]
        }).catch(error => {
            console.log(error);
        })
})

</script>
<style lang="scss" scoped>
.footer-image{
    height: 96px;
}
.social-link{
    // @apply h-10 d-flex justify-content-center align-items-center text-white w-10 bg-success rounded-full
    height: 40px;
    width: 40px;
    border-radius: 100%;
}
.bg-blue{
    background-color: rgb(55, 165, 255);
}
.bg-red{
    background-color: rgb(255, 85, 55);
}
.bg-main-color{
    background: #FD820E;
}
.main-color{
    color: #FD820E;
}
// footer {
//     background-color: #222222;

//     .logo {
//         img {
//             width: 150px !important;
//         }
//     }

//     .links {
//         li {
//             a {
//                 position: relative;
//                 transition: 0.2s;

//                 &::before {
//                     content: "";
//                     position: absolute;
//                     transition: 0.2s;
//                     width: 0;
//                     height: 3px;
//                     background-color: var(--blue-color);
//                     bottom: -5px;
//                     left: 50%;
//                     transform: translateX(-50%);
//                     border-radius: 50px;
//                 }

//                 &:hover {
//                     color: var(--blue-color) !important;
//                 }

//                 &:hover::before {
//                     width: 100%;
//                 }
//             }
//         }
//     }

//     .contacts-info {
//         a {
//             text-decoration: none;
//             transition: 0.2s;

//             i {
//                 position: relative;
//                 top: 5px;
//             }

//             &:hover {
//                 color: var(--blue-color) !important;
//             }
//         }
//     }

//     .copyright {
//         font-size: 13px;

//         a {
//             color: var(--orange-color);
//             text-decoration: none;

//             &:hover {
//                 text-decoration: underline;
//             }
//         }
//     }

//     @media (max-width: 991px) {
//         .footer-cont {
//             flex-wrap: wrap;
//         }
//     }

//     @media (max-width: 767px) {
//         .footer-cont {
//             justify-content: center !important;
//             flex-direction: column;
//             align-items: center;

//             ul {
//                 flex-direction: column;
//                 text-align: center;
//             }
//         }
//     }
// }
</style>