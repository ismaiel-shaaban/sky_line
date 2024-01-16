<template>

  <footer>
    <section class="col-10 mx-auto my-3">
      <div
        class="d-flex flex-wrap align-items-center justify-content-lg-between justify-center"
      >
        <div class="col-3 mt-lg-0 my-2">
          <img
            src="../../public/images/logo.png"
            class="footer-image"
            alt=""
          />
        </div>
        <div class="d-flex col-lg gap-3 justify-content-between w-100">
          <div
            class="d-flex justify-content-center align-items-center text-white bg-success social-link"
          >
            <i class="fa-brands fa-whatsapp fs-4"></i>
          </div>
          <div
            class="d-flex justify-content-center align-items-center text-white bg-red social-link"
          >
            <i class="fa-brands fa-instagram fs-4"></i>
          </div>
          <div
            class="d-flex justify-content-center align-items-center text-white bg-blue social-link"
          >
            <i class="fa-brands fa-twitter fs-4"></i>
          </div>
          <div
            class="d-flex justify-content-center align-items-center text-white bg-primary social-link"
          >
            <i class="fa-brands fa-facebook-f fs-4"></i>
          </div>
          <div
            class="d-flex justify-content-center align-items-center text-white bg-warning social-link"
          >
            <i class="fa-brands fa-snapchat fs-4"></i>
          </div>
          <div
            class="d-flex justify-content-center align-items-center text-white bg-black social-link"
          >
            <i class="fa-brands fa-tiktok fs-4"></i>
          </div>
          <div
            class="d-flex justify-content-center align-items-center text-white bg-danger social-link"
          >
            <i class="fa-brands fa-youtube fs-4"></i>
          </div>
        </div>
      </div>
    </section>
    <section class="d-flex flex-wrap col-10 mx-auto my-5">
      <div class="col-lg-4 col-md-6">
        <h3 class="text-3xl font-semibold main-color">
          {{ $t("footer.address.tit") }}
        </h3>
        <h5 class="fw-semibold my-2 mt-4">
          {{ $t("footer.address.details") }}
        </h5>
        <h5 class="fw-semibold my-2">{{ $t("footer.address.tel") }}</h5>
        <h5 class="fw-semibold my-2">{{ $t("footer.address.email") }}</h5>
      </div>
      <!-- <div class="col-lg-4 text-center col-md-6">
        <h3 class="text-3xl font-semibold main-color">
          {{ $t("footer.linksTit") }}
        </h3>
        <ul class="mt-4">
          <template v-for="(item, index) in $tm('footer.links')" :key="index">
            <li class="fs-5 fw-semibold my-3">{{ item }}</li>
          </template>
        </ul>
      </div> -->
      <div class="col-lg-4 col-md-6 text-center">
        <!-- <i class="fa-solid fa-phone main-color contact-sec fs-2"></i> -->
        <h3 class="text-2xl font-bold main-color mb-4 text-gray-800">
          {{ $t("home.sec9.gorg.tit") }}
        </h3>
        <template
          v-for="(item, index) in $tm('home.sec9.gorg.tel')"
          :key="index"
        >
          <h4 class="mb-2">
            <i class="fa-solid fa-phone text-primary ms-3"></i
            ><span class="text-xl font-semibold">{{ item }}</span>
          </h4>
        </template>
      </div>
    </section>
    <section class="bg-main-color py-2 text-center">
      <p class="fs-5 fw-semibold text-white">{{ $t("footer.para") }}</p>
    </section>
  </footer>
</template>
<script setup>
import { useRouter } from "vue-router";
import { ref, onMounted } from "vue";
import axios from "axios";

const router = useRouter();
const info = ref([]);

onMounted(async () => {
  await axios
    .get("https://seasonreal.seasonsge.com/appv1real/info")
    .then((data) => {
      info.value = data.data[0];
    })
    .catch((error) => {
      console.log(error);
    });
});
</script>
<style lang="scss" scoped>
.footer-image {
  height: 96px;
}
.social-link {
  // @apply h-10 d-flex justify-content-center align-items-center text-white w-10 bg-success rounded-full
  height: 40px;
  width: 40px;
  border-radius: 100%;
}
.bg-blue {
  background-color: rgb(55, 165, 255);
}
.bg-red {
  background-color: rgb(255, 85, 55);
}
.bg-main-color {
  background: #fd820e;
}
.main-color {
  color: #fd820e;
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
