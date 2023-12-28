<template>
    <div class="home-page">
        <NewPopup :info="info" :openPopup="newPopup" @close-newPopup="() => (newPopup = false)"></NewPopup>
        <HeaderComp class=" top-0 bg-white w-100" style="z-index: 555"></HeaderComp>
        <!-- <div class="landing min-vh-100">
            <Carousel class="min-vh-100 m-0 position-relative" :autoplay="3000" :wrap-around="true"
                :dir="$i18n.locale === 'en' ? 'ltr' : 'rtl'">
                <Slide class="min-vh-100 w-100 m-0" v-for="(item, index) in slider" :key="index">
                    <div class="carousel__item w-100 h-100 m-0">
                        <img :src="`https://seasonreal.seasonsge.com/images/settings/${item.image}`" class="d-block w-100 vh-100"
                            style="object-fit: cover;" alt="..." />
                        <div :class="`container text-${$i18n.locale === 'en' ? 'start' : 'end'}`">
                            {{ item["title-en"] }}
                            <div :class="`text-box p-4 position-absolute rounded-5 ${$i18n.locale === 'ar' ? 'ar' : ''}`"
                                v-html="$i18n.locale === 'en' ? item['title_en'] : item['title']"></div>
                        </div>
                    </div>
                </Slide>
                <template #addons>
                    <Navigation />
                    <Pagination class="position-absolute" />
                </template>
            </Carousel>
            <div class="socials d-flex align-items-center gap-3 position-absolute">
                <a target="_blank" :href="info.facebook">
                    <i class="fa-brands fa-facebook text-white fs-5"></i>
                </a>
                <a target="_blank" :href="info.messenger">
                    <i class="fa-brands fa-facebook-messenger text-white fs-5"></i>
                </a>
                <a target="_blank" :href="info.twitter">
                    <i class="fa-brands fa-twitter text-white fs-5"></i>
                </a>
                <a target="_blank" :href="info.telegram">
                    <i class="fa-brands fa-telegram text-white fs-5"></i>
                </a>
                <a target="_blank" :href="info.instagram">
                    <i class="fa-brands fa-instagram text-white fs-5"></i>
                </a>
                <a target="_blank" :href="info.youtube">
                    <i class="fa-brands fa-youtube text-white fs-5"></i>
                </a>
                <a target="_blank" :href="info.tiktok">
                    <i class="fa-brands fa-tiktok text-white fs-5"></i>
                </a>
                <a target="_blank" :href="info.whatsapp">
                    <i class="fa-brands fa-whatsapp text-white fs-5"></i>
                </a>
                <a target="_blank" :href="info.snapchat">
                    <i class="fa-brands fa-snapchat text-white fs-5"></i>
                </a>
            </div>
        </div> -->
        <section class="my-5">
            <div class="row mx-auto d-flex col-10  flex justify-content-between align-items-center">
            <div class="col-lg-6 lg:text-start text-center">
                <h1 class="text-3xl main-color font-semibold">{{$t('home.sec1.tit')}}</h1>
                <h5 class="text-lg text-gray-600 font-semibold mt-3">{{ $t('home.sec1.para') }}</h5>
            </div>
            <div class="col-lg-6 w-full lg:mt-0 mt-3">
                <div class="w-50 mx-auto d-flex  flex justify-content-center align-items-center"><img src="../assets/Images/sky-logo.png" class="w-50 lg:ms-auto mx-auto" alt=""></div>
            </div>
            </div>
        </section>
        <section class="my-5">
            <h1 class="text-3xl main-color text-center font-semibold">{{ $t('home.sec2.tit') }}</h1>
            <h4 class="text-lg text-gray-600 col-8 text-center mx-auto mt-5">{{ $t('home.sec2.para') }}</h4>
        </section>
        <section class="my-5">
            <h1 class="text-center main-color">{{ $t('home.sec3.tit') }}</h1>
            <div class="d-flex flex-wrap col-10 mx-auto mt-5">
                <div class="col-lg-4 col-md-6 col-12 mt-3 px-3">
                    <div class="card position-relative pb-4">
                    <img src="../assets/Images/10Days.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="m-0 text-decoration-line-through fw-bold text-center text-lg">1235</p>
                        <p class="m-0 font-semibold fw-bold text-center">1280</p>
                        <p class="m-0 text-center text-sm fw-bold">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">{{ $t('home.sec3.card1.cardtit') }}</h6>
                    <p class="text-center text-gray-600 my-1 mb-2">{{ $t('home.sec3.card1.cardpara') }}</p>
                    <button class="prim-btn col-10 mx-auto"><i class="fa-brands fa-whatsapp me-3"></i>{{ $t('home.sec3.card1.cardbtn') }}</button>
                    </div>
                </div>
                <div class="col-lg-4 col-md-6 col-12 mt-3 px-3">
                    <div class="card position-relative pb-4">
                    <img src="../assets/Images/8Days.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-bold m-0 text-decoration-line-through text-gray-400 text-center text-lg">1055</p>
                        <p class="fw-bold m-0 text-lg font-semibold text-center">1050</p>
                        <p class="fw-bold m-0 text-center text-sm">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">{{ $t('home.sec3.card2.cardtit') }}</h6>
                    <p class="text-center text-gray-600 my-1 mb-2">{{ $t('home.sec3.card2.cardpara') }}</p>
                    <button class="prim-btn col-10 mx-auto"><i class="fa-brands fa-whatsapp me-3"></i>{{ $t('home.sec3.card2.cardbtn') }}</button>
                    </div>
                </div>
                <div class="col-lg-4 col-md-6 col-12 mt-3 px-3">
                    <div class="card position-relative pb-4">
                    <img src="../assets/Images/12Days.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-bold m-0 text-decoration-line-through text-gray-400 text-center text-lg">1485</p>
                        <p class="fw-bold m-0 text-lg font-semibold text-center">1590</p>
                        <p class="fw-bold m-0 text-center text-sm">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">{{ $t('home.sec3.card3.cardtit') }}</h6>
                    <p class="text-center text-gray-600 my-1 mb-2">{{ $t('home.sec3.card3.cardpara') }}</p>
                    <button class="prim-btn col-10 mx-auto"><i class="fa-brands fa-whatsapp me-3"></i>{{ $t('home.sec3.card1.cardbtn') }}</button>
                    </div>
                </div>
            </div>
        </section>
        <section class="my-5 img-overlay d-flex justify-content-center align-items-center">
          <div class="d-flex flex-wrap align-items-center col-lg-6 col-md-8 col-10 text-center justify-content-between">
            <h3 class="fw-semibold col-lg-6 text-white">{{ $t('home.sec4.tit') }}</h3>
            <button class="btn btn-light col-lg-6 lg:mt-0 mt-3 fw-semibold text-lg"><i class="fa-brands fa-whatsapp me-3 text-success"></i>{{ $t('home.sec4.btn') }}</button>
          </div>
        </section>
        <section class="my-5">
            <h2 class="fw-semibold main-color text-center">{{ $t('home.sec5.tit') }}</h2>
            <h6 class="fw-semibold col-6 mx-auto text-center mt-3">{{ $t('home.sec5.para') }}</h6>
        </section>
        <section class="my-5">
            <h1 class="text-5xl font-semibold text-center main-color">{{ $t('home.sec6.tit') }}</h1>
            <div class="d-flex flex-wrap col-10 mx-auto mt-7">
                <div class="col-lg-4 col-md-6 col-12 mt-3 px-3">
                    <div class="card position-relative pb-4">
                    <img src="../assets/Images/12Days-azrabegan.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">1280</p>
                        <p class="fw-semibold m-0 text-center">1630</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">{{ $t('home.sec6.card1.cardtit') }}</h6>
                    <p class="text-center text-gray-600 my-3">{{ $t('home.sec6.card1.cardpara') }}</p>
                    <button class="prim-btn rounded-3xl w-10/12 block mx-auto font-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                    </div>
                </div>
                <div class="col-lg-4 col-md-6 col-12 mt-3 px-3">
                    <div class="card relative pb-4">
                    <img src="../assets/Images/10Days-azrabegan.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">1110</p>
                        <p class="fw-semibold m-0 text-lg font-semibold text-center">1420</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">{{ $t('home.sec6.card2.cardtit') }}</h6>
                    <p class="text-center text-gray-600 my-3">{{ $t('home.sec6.card2.cardpara') }}</p>
                    <button class="prim-btn w-10/12 block mx-auto font-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                    </div>
                </div>
                <div class="col-lg-4 col-md-6 col-12 mt-3 px-3">
                    <div class="card position-relative pb-4">
                    <img src="../assets/Images/8Days-azrabegan.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">940</p>
                        <p class="fw-semibold m-0 text-center">1210</p>
                        <p class="fw-semibold m-0 text-center text-sm">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">{{ $t('home.sec6.card3.cardtit') }}</h6>
                    <p class="text-center text-gray-600 my-3">{{ $t('home.sec6.card3.cardpara') }}</p>
                    <button class="prim-btn w-10/12 block mx-auto font-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                    </div>
                </div>
            </div>
        </section>
        <!-- <section class="mt-5 my-5 position-relative pt-5 d-none d-md-block">
            <div class="img-overlay2"></div>
            <h6 class="text-center col-7 position-relative z-10 my-5 mx-auto">نسعي الي نقل السياحة في جورجيا و اذربيجان الي افضل وارقي مستوي بأنسب الاسعار . سياحتكم في امان مع سكاي لاين الاسم الاضمن و الاشهر في مجال السياحة في دولتين جورجيا و اذربيجان</h6>
            <div class="card position-relative z-10 col-10 mx-auto pb-4 d-flex flex-wrap justify-content-lg-between justify-content-center">
                <img src="../assets/Images/10Days.png" class="card-image" alt="">
                <div class="price-overlay">
                    <p class="fw-semibold m-0 text-decoration-line-through text-center">1235</p>
                    <p class="fw-semibold m-0 text-center">1280</p>
                    <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                </div>
                <div class="d-flex flex-wrap w-full my-lg-2 mt-1">
                    <h6 class=" ms-5 fw-semibold px-2 col-6 text-lg-start text-center">برنامج ❄️ جورجيا السياحي 10 ايام 9 ليالي العرض الذهبي</h6>
                    <h6 class=" me-5 text-lg-end col-lg-4 fw-semibold text-center">10 ايام و 9 ليالى</h6>
                </div>
                <div class="d-flex flex-wrap w-full justify-content-lg-between justify-content-center">
                    <h6 class="w-5/12 ms-3 fw-semibold d-lg-block d-hidden">برنامج ❄️ جورجيا السياحي 10 ايام 9 ليالي العرض الذهبي</h6>
                    <button class="prim-btn rounded-3xl col-lg-4 col-10 me-lg-5 d-block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                </div>
            </div>
        </section>
        <section class="mb-5 d-none d-md-block">
            <div class="d-flex flex-wrap my-5 col-10 mx-auto mt-5">
                <div class="col-lg-4 col-md-6 px-3 mt-5">
                    <div class="card position-relative pb-4">
                    <img src="../assets/Images/8Days.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">1055</p>
                        <p class="fw-semibold m-0 text-center">1050</p>
                        <p class="fw-semibold m-0 text-center text-sm">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">برنامج ❄️ جورجيا السياحي 8 ايام 7 ليالي العرض الذهبي</h6>
                    <p class="text-center my-1 mb-2">8 ايام و 7 ليالى</p>
                    <button class="prim-btn col-10 d-block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                    </div>
                </div>
                <div class="col-lg-4 col-md-6 px-3 mt-5">
                    <div class="card position-relative pb-4">
                    <img src="../assets/Images/12Days.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">1485</p>
                        <p class="fw-semibold m-0 text-center">1590</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">برنامج ❄️ جورجيا السياحي 12 يوم 11 ليلة العرض الذهبي</h6>
                    <p class="text-center my-1 mb-2">12 ايام و 11 ليالى</p>
                    <button class="prim-btn col-10 d-block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                    </div>
                </div>
                <div class="col-lg-4 col-md-6 px-3 mt-5">
                    <div class="card position-relative pb-4">
                    <img src="../assets/Images/12Days-azrabegan.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-center text-decoration-line-through">1280</p>
                        <p class="fw-semibold m-0 text-center">1630</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">برنامج اذربيجان السياحي 12 يوم 11 ليلة العرض الذهبي❄️</h6>
                    <p class="text-center my-1 mb-2">12 ايام و 11 ليالى</p>
                    <button class="prim-btn col-10 d-block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                    </div>
                </div>
                <div class="col-lg-4 col-md-6 px-3 mt-5">
                    <div class="card position-relative pb-4">
                    <img src="../assets/Images/10Days-azrabegan.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-center text-decoration-line-through">1110</p>
                        <p class="fw-semibold m-0 text-center">1420</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">برنامج اذربيجان السياحي 10 ايام 9 ليالي العرض الذهبي❄️</h6>
                    <p class="text-center my-1 mb-2">10 ايام و 9 ليالى</p>
                    <button class="prim-btn col-10 d-block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                    </div>
                </div>
                <div class="col-lg-4 col-md-6 px-3 mt-5">
                    <div class="card position-relative pb-4">
                    <img src="../assets/Images/8Days-azrabegan.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-center text-decoration-line-through">940</p>
                        <p class="fw-semibold m-0 text-center">1210</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">برنامج اذربيجان السياحي 8 ايام 7 ليالي العرض الذهبي❄️</h6>
                    <p class="text-center my-1 mb-2">8 ايام و 7 ليالى</p>
                    <button class="prim-btn col-10 d-block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                    </div>
                </div>
            </div>
        </section>
        <section class="my-10 position-relative pt-5 d-block d-md-none">
            <div class="img-overlay2"></div>
            <p class="text-center col-7 position-relative z-10 my-3 mx-auto">نسعي الي نقل السياحة في جورجيا و اذربيجان الي افضل وارقي مستوي بأنسب الاسعار . سياحتكم في امان مع سكاي لاين الاسم الاضمن و الاشهر في مجال السياحة في دولتين جورجيا و اذربيجان</p>
            <swiper :modules="modules" :slides-per-view="1" :loop="true" :autoplay="{delay:2500,diableOnInteraction:false,pauseOnMouseEnter:true}" :navigation="true" :pagination="{clickable: true,}"  :space-between="50" @swiper="onSwiper" @slideChange="onSlideChange" class="w-100 text-center">
                <swiper-slide>
                <div class="card mb-5 position-relative z-10 col-10 mx-auto pb-4">
                    <img src="../assets/Images/10Days.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">1235</p>
                        <p class="fw-semibold m-0 text-center">1280</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h2 class="card-title">برنامج ❄️ جورجيا السياحي 10 ايام 9 ليالي العرض الذهبي</h2>
                    <p class="text-center text-gray-600 my-3">10 ايام و 9 ليالى</p>
                    <button class="prim-btn col-10 block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                </div>
                </swiper-slide>
                <swiper-slide>
                <div class="card position-relative z-10 col-10 mx-auto pb-4">
                    <img src="../assets/Images/8Days.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">1055</p>
                        <p class="fw-semibold m-0 text-center">1050</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">برنامج ❄️ جورجيا السياحي 8 ايام 7 ليالي العرض الذهبي</h6>
                    <p class="text-center my-1 mb-2">8 ايام و 7 ليالى</p>
                    <button class="prim-btn col-10 block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                </div>
                </swiper-slide>
                <swiper-slide>
                <div class="card position-relative z-10 col-10 mx-auto pb-4">
                    <img src="../assets/Images/12Days.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">1485</p>
                        <p class="fw-semibold m-0 text-center">1590</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">برنامج ❄️ جورجيا السياحي 12 يوم 11 ليلة العرض الذهبي</h6>
                    <p class="text-center my-1 mb-2">12 ايام و 11 ليالى</p>
                    <button class="prim-btn col-10 block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                </div>
                </swiper-slide>
                <swiper-slide>
                <div class="card position-relative z-10 col-10 mx-auto pb-4">
                    <img src="../assets/Images/12Days-azrabegan.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">1280</p>
                        <p class="fw-semibold m-0 text-center">1630</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">برنامج اذربيجان السياحي 12 يوم 11 ليلة العرض الذهبي❄️</h6>
                    <p class="text-center my-1 mb-2">12 ايام و 11 ليالى</p>
                    <button class="prim-btn col-10 block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                </div>
                </swiper-slide>
                <swiper-slide>
                <div class="card position-relative z-10 col-10 mx-auto pb-4">
                    <img src="../assets/Images/10Days-azrabegan.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">1110</p>
                        <p class="fw-semibold m-0 text-center">1420</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">برنامج اذربيجان السياحي 10 ايام 9 ليالي العرض الذهبي❄️</h6>
                    <p class="text-center my-1 mb-2">10 ايام و 9 ليالى</p>
                    <button class="prim-btn col-10 block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                </div>
                </swiper-slide>
                <swiper-slide>
                <div class="card position-relative z-10 col-10 mx-auto pb-4">
                    <img src="../assets/Images/8Days-azrabegan.png" class="card-image" alt="">
                    <div class="price-overlay">
                        <p class="fw-semibold m-0 text-decoration-line-through text-center">940</p>
                        <p class="fw-semibold m-0 text-center">1210</p>
                        <p class="fw-semibold m-0 text-center">{{ $t('home.money') }}</p>
                    </div>
                    <h6 class="text-center">برنامج اذربيجان السياحي 8 ايام 7 ليالي العرض الذهبي❄️</h6>
                    <p class="text-center my-1 mb-2">8 ايام و 7 ليالى</p>
                    <button class="prim-btn col-10 block mx-auto fw-semibold"><i class="fa-brands fa-whatsapp me-3"></i>استفسر واحجز واتساب</button>
                </div>
                </swiper-slide>
            </swiper>
        </section> -->
        <!-- <div class="apps-section py-5">
            <div class="container">
                <div class="heading-text">
                    <h1>{{ $t('tourApps.heading') }}</h1>
                    <p class="text-black-50 w-75 mx-auto fs-5">
                        {{ $t('tourApps.paragraph') }}
                    </p>
                </div>
                <div class="apps d-flex align-items-center justify-content-center gap-5 mt-5">
                    <a target="_blank" :href="info.google_play_link">
                        <img class="img-fluid" src="/images/googleplay.png" alt="" />
                    </a>
                    <a target="_blank" :href="info.app_store_link">
                        <img class="img-fluid" src="/images/appstore.png" alt="" />
                    </a>
                </div>
                <div class="text-center mt-5">
                    <button class="butn p-2 px-4 rounded-1 text-decoration-none fs-5" @click="aboutPopup = true">
                        {{ $t('buttons.readMore') }}
                    </button>
                </div>
                <AboutPopUp :openPopup="aboutPopup" @close-aboutPopup="() => (aboutPopup = false)"></AboutPopUp>
            </div>
        </div> -->
        <!-- <div class="reservation-section py-5">
            <div class="container">
                <div class="heading-text">
                    <h1>{{ $t('reservation.heading') }}</h1>
                    <p class="text-black-50 fs-5">
                        {{ $t('reservation.paragraph') }}
                    </p>
                </div>
                <form class="search-form mt-5 d-flex justify-content-center align-items-md-start gap-2">
                    <div class="input-cont position-relative w-50">
                        <input
                            :class="`search-input w-100 px-3 p-2 rounded-1 ${validation.searchInput.$error ? 'error' : ''}`"
                            type="search" placeholder="e.g. 2alw2m5lfwlc4ockk0kw" v-model="searchForm.searchInput" />
                        <span v-if="validation.searchInput.$error" class="text-danger fst-italic d-block mt-1">
                            {{ validation.searchInput.required.$message }}
                        </span>
                        <span v-if="searchError !== ''" class="text-danger fst-italic d-block mt-1">
                            {{ searchError }}
                        </span>
                    </div>
                    <button class="butn p-2 px-3 rounded-1 d-flex align-items-center gap-2" type="submit"
                        @click.prevent="search">
                        <i class="fa-solid fa-magnifying-glass"></i>
                        {{ $t('buttons.search') }}
                    </button>
                </form>
            </div>
        </div> -->
        <!-- <div class="services-section py-5">
            <div class="container">
                <div class="heading-text">
                    <h1>{{ $t('services.heading') }}</h1>
                    <p class="text-black-50 w-75 mx-auto fs-5">
                        {{ $t('services.paragraph') }}
                    </p>
                </div>
                <div class="box-cont mt-5">
                    <div class="row">
                        <div class="col-md-6 mb-4" v-for="(item, index) in $tm('serviciesCards')" :key="index">
                            <div class="box overflow-hidden bg-white rounded-2 d-flex flex-column h-100">
                                <div class="image">
                                    <router-link v-if="!item.link.includes('http')" :to="`/${$i18n.locale}/${item.link}`">
                                        <img v-if="images[index]"  class="img-fluid w-100" :src="`https://seasonreal.seasonsge.com/appv1real/${images[index+1].image}`" alt="" />
                                    </router-link>
                                    <a v-if="item.link.includes('http')" target="_blank" :href="item.link">
                                        <img v-if="images[index]" class="img-fluid w-100" :src="`https://seasonreal.seasonsge.com/appv1real/${images[index].image}`" alt="" />
                                    </a>
                                </div>
                                <div class="text flex-fill d-flex flex-column justify-content-between p-4">
                                    <div class="txt">
                                        <h3>{{ item.heading }}</h3>
                                        <p class="text-black-50 mt-3">
                                            {{ item.paragraph }}
                                        </p>
                                    </div>
                                    <router-link v-if="!item.link.includes('http')" class="fw-bold"
                                        :to="`/${$i18n.locale}/${item.link}`">
                                        {{ $t('buttons.bookNow') }}
                                        {{ $i18n.locale === "en" ? "&rightarrow;" : "&leftarrow;" }}
                                    </router-link>
                                    <a v-if="item.link.includes('http')" target="_blank" :href="item.link" class="fw-bold">
                                        {{ $t('buttons.bookNow') }}
                                        {{ $i18n.locale === "en" ? "&rightarrow;" : "&leftarrow;" }}
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div> -->
        <!-- <div class="offers-section position-relative py-5">
            <img class="position-absolute" src="/images/sales.png" alt="" />
            <div class="container">
                <div class="heading-text">
                    <h1>{{ $t('offers.heading') }}</h1>
                    <p class="text-black-50 w-75 mx-auto fs-5 mb-5">
                        {{ $t('offers.paragraph') }}
                    </p>
                    <button class="butn p-2 px-4 rounded-1 text-decoration-none fs-5" @click="offersPopup = true">
                        {{ $t('buttons.readMore') }}
                    </button>
                </div>
                <OffersPopup :openPopup="offersPopup" @close-offersPopup="() => offersPopup = false"></OffersPopup>
            </div>
        </div> -->
        <section ref="targetDiv" class="border-bottom border-black my-5" id="createDiv">
            <div class="col-10 mx-auto my-5">
                <div class="d-flex flex-wrap justify-content-between">
                    <div class="text-center col-lg-3 col-md-6 mt-3" v-for="(item, index) in $tm('serviciesCards')" :key="index">
                        <router-link v-if="!item.link.includes('http')" class="fw-bold text-decoration-none"
                        :to="`/${$i18n.locale}/${item.link}`">
                            <div class="circle-shadow-o" v-if="index == 0"><i class="fa-solid fa-shield text-white fs-1"></i></div>
                            <div class="circle-shadow-b" v-else-if="index == 1"><i class="fa-solid fa-hotel text-white fs-1"></i></div>
                            <div class="circle-shadow-o" v-else-if="index == 2"><i class="fa-solid fa-car-side text-white fs-1"></i></div>
                            <h3 class="text-2xl mt-5 fw-bold text-decoration-underline">{{item.heading }}</h3>
                        </router-link>
                        <a v-if="item.link.includes('http')" target="_blank" class="fw-bold"
                        :href="item.link">
                            <div class="circle-shadow-b"><i class="fa-sharp fa-solid fa-train text-white fs-1"></i></div>
                            <h3 class="text-2xl mt-5 fw-bold">{{item.heading }}</h3>
                        </a>
                    </div>
                    <!-- <div class="text-center col-lg-3 col-md-6 mt-3">
                    <div class="circle-shadow-b"><i class="fa-solid fa-hotel text-white fs-1"></i></div>
                    <a href=""><h3 class="text-2xl mt-5 ">{{ $t('serviciesCards[1].heading') }}</h3></a>
                    </div>
                    <div class="text-center col-lg-3 col-md-6 mt-3">
                    <div class="circle-shadow-o"><i class="fa-solid fa-car-side text-white fs-1"></i></div>
                    <a href=""><h3 class="text-2xl mt-5 ">{{ $t('serviciesCards[2].heading') }}</h3></a>
                    </div>
                    <div class="text-center col-lg-3 col-md-6 mt-3">
                    <div class="circle-shadow-b"><i class="fa-sharp fa-solid fa-train text-white fs-1"></i></div>
                    <a href=""><h3 class="text-2xl mt-5 ">{{ $t('serviciesCards[3].heading') }}</h3></a>
                    </div> -->
                </div>
            </div>
        </section>
        <Loader v-if="loading"></Loader>
        <section class="bg-main-color py-5 d-flex justify-content-center align-items-center mb-5">
            <div class="d-flex flex-wrap col-10 justify-content-between">
                <h3 class="fw-bold col-md-6 text-center text-white">{{ $t('home.sec7.tit') }}</h3>
                <button class="btn btn-light col-md-6 mt-md-0 mt-3 fw-semibold"><i class="fa-solid fa-comments me-5"></i>{{ $t('home.sec7.btn') }}</button>
            </div>
        </section>
        <section class="my-10">
            <swiper :modules="modules" :slides-per-view="numOfImage" :loop="true" :autoplay="{delay:1000,diableOnInteraction:false,pauseOnMouseEnter:true}"  :space-between="50" @swiper="onSwiper" @slideChange="onSlideChange" class=" px-5 d-flex justify-content-center">
                <swiper-slide><img src="../assets/Images/image1.png" class="w-100" alt=""></swiper-slide>
                <swiper-slide><img src="../assets/Images/image2.png" class="w-100" alt=""></swiper-slide>
                <swiper-slide><img src="../assets/Images/image3.png" class="w-100" alt=""></swiper-slide>
                <swiper-slide><img src="../assets/Images/image4.png" class="w-100" alt=""></swiper-slide>
                <swiper-slide><img src="../assets/Images/image5.png" class="w-100" alt=""></swiper-slide>
                <swiper-slide><img src="../assets/Images/image6.png" class="w-100" alt=""></swiper-slide>
                <swiper-slide><img src="../assets/Images/image7.png" class="w-100" alt=""></swiper-slide>
                <swiper-slide><img src="../assets/Images/image8.png" class="w-100" alt=""></swiper-slide>
                <swiper-slide><img src="../assets/Images/image9.png" class="w-100" alt=""></swiper-slide>
            </swiper>
        </section>
        <section class="bg-main-color py-5 d-flex justify-content-center align-items-center my-5">
            <div class="d-flex flex-wrap col-10 justify-content-md-between justify-center align-items-center">
                <h3 class="fw-bold col-md-6 text-center text-white">{{ $t('home.sec8.tit') }}</h3>
                <button @click="scrollToDiv" class="btn btn-light col-md-6 mt-md-0 mt-3 fw-semibold" >{{ $t('home.sec8.btn') }}</button>
            </div>
        </section>  
        <section class="d-flex flex-wrap col-10 mx-auto justify-content-lg-between justify-center">
            <div class="col-lg-4 col-md-6 text-center">
                <i class="fa-solid fa-phone main-color contact-sec fs-2"></i>
                <h3 class="text-2xl font-bold my-5 text-gray-800">{{ $t('home.sec9.azra.tit') }}</h3>
                <h4><i class="fa-solid fa-phone main-color ms-3"></i><span class="text-xl font-semibold text-gray-500">{{ $t('home.sec9.azra.tel') }}</span></h4>
            </div>
            <div class="col-lg-4 col-md-6 text-center">
                <i class="fa-solid fa-phone main-color contact-sec fs-2"></i>
                <h3 class="text-2xl font-bold my-5 text-gray-800">{{ $t('home.sec9.gorg.tit') }}</h3>
                <template v-for="item,index in $tm('home.sec9.gorg.tel')" :key="index">
                    <h4 class="mb-2"><i class="fa-solid fa-phone main-color ms-3"></i><span class="text-xl font-semibold">{{ item }}</span></h4>
                </template>
            </div>
            <div class="col-lg-4 col-md-6 text-center">
                <i class="fa-solid fa-phone main-color contact-sec fs-2"></i>
                <h3 class="text-2xl font-bold my-5 text-gray-800">{{ $t('home.sec9.sud.tit') }}</h3>
                <h4><i class="fa-solid fa-phone main-color ms-3"></i><span class="text-xl font-semibold text-gray-500">{{ $t('home.sec9.sud.tel') }}</span></h4>
            </div>
        </section>
        <FooterComp></FooterComp>
    </div>
</template>
<script setup>
import HeaderComp from "../components/HeaderComp.vue";
import FooterComp from "../components/FooterComp.vue";
// import AboutPopUp from "../components/AboutPopUp.vue";
import OffersPopup from "../components/OffersPopup.vue";
import NewPopup from "../components/NewPopup.vue";
import { ref, watch, onMounted, inject } from "vue";
import axios from "axios";
import i18n from "../i18n";
import { Carousel, Slide } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'
import router from "../router";
import Loader from "../components/Loader.vue";
import { useVuelidate } from "@vuelidate/core";
import { required, helpers } from "@vuelidate/validators";
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
// import 'path-to-your-style/style.css'; // replace with the correct path

// Import required modules
import { Autoplay, Pagination, Navigation } from 'swiper/modules';

const modules = ref([Autoplay, Pagination, Navigation]);

const slider = ref([]);
const images = ref([]);
const newPopup = ref(false);
const aboutPopup = ref(false);
const offersPopup = ref(false);
const info = ref([]);
const loading = ref(false)
const searchError = ref('')
const numOfImage = ref('4')
const searchForm = ref({
    searchInput: '',
})
const targetDiv = ref(null);
const scrollToDiv = ()=>{
        if (targetDiv.value) {
            targetDiv.value.scrollIntoView({ behavior: 'smooth' });
      }
    }
const rules = {
    searchInput: { required: helpers.withMessage("Required Field", required) },
}
const validation = useVuelidate(rules, searchForm)

const search = async () => {
    validation.value.$validate()
    if (!validation.value.$error) {
        loading.value = true
        const formData = new FormData()
        formData.append('searchValue' ,searchForm.value.searchInput)
        await axios.post(`https://seasonreal.seasonsge.com/appv1real/booking_search`,formData)
            .then(data => {
                console.log("data" , data);

                if (data.data.bookings && data.data.bookings.length > 0) {
                    const carsBooking = data.data.bookings[0]
                    axios.get(`https://seasonreal.seasonsge.com/appv1real/user-data?user_id=${carsBooking.account_owner}`)
                        .then(data => {
                            loading.value = false
                            if (data.data.type == 2) {
                                router.push({
                                    name: 'Cars Checkout',
                                    params: { lang: i18n.global.locale.value, id: carsBooking.random_code ,with:1 }
                                })
                            } else if (data.data.type == 1) {
                                router.push({
                                    name: 'Agents Cars Checkout',
                                    params: { lang: i18n.global.locale.value, id: carsBooking.random_code, with: 2 }
                                    
                                })
                            }
                           
                        })
                        setTimeout(() => {
                                  
                            window.location.reload()
                        }, 1000)
                } else if (data.data.bookingss && data.data.bookingss.length > 0) {
                    const flightsBooking = data.data.bookingss[0]
                    axios.get(`https://seasonreal.seasonsge.com/appv1real/user-data?user_id=${flightsBooking.email}`)
                        .then(data => {
                            loading.value = false
                            if (data.data.type == 2) {
                                router.push({
                                    name: 'Flights Checkout',
                                    params: { lang: i18n.global.locale.value, id: flightsBooking.booking_id , with: 1}
                                })
                            } else if (data.data.type == 1) {
                                router.push({
                                    name: 'Agents Flights Checkout',
                                    params: { lang: i18n.global.locale.value, id: flightsBooking.booking_id, with: 2 }
                                })
                            }
                        })
                        setTimeout(() => {
                                  
                                  window.location.reload()
                        }, 1000)
                } else if (data.data.hotel_reservations && data.data.hotel_reservations.length > 0) {
                    const HotelsBooking = data.data.hotel_reservations[0]
                    axios.get(`https://seasonreal.seasonsge.com/appv1real/user-data?user_id=${HotelsBooking.account_name}`)
                        .then(data => {
                            loading.value = false
                            if (data.data.type == 2) {
                                router.push({
                                    name: 'Hotels Checkout',
                                    params: { lang: i18n.global.locale.value, id: HotelsBooking.code , with: 1}
                                })
                            } else if (data.data.type == 1) {
                                router.push({
                                    name: 'Agents Hotels Checkout',
                                    params: { lang: i18n.global.locale.value, id: HotelsBooking.code, with: 2}
                                })
                            }
                        })
                        setTimeout(() => {
                                  
                                  window.location.reload()
                        }, 1000)
                } else if (data.data.book && data.data.book.length > 0) {
                    const ProgramsBooking = data.data.book[0]
                    axios.get(`https://seasonreal.seasonsge.com/appv1real/user-data?user_id=${ProgramsBooking.email}`)
                        .then(data => {
                            loading.value = false
                            if (data.data.type == 2) {
                                router.push({
                                    name: 'Programs Checkout',
                                    params: { lang: i18n.global.locale.value, id: ProgramsBooking.booking_id , with: 1 }
                                })
                            } else if (data.data.type == 1) {
                                router.push({
                                    name: 'Agents Programs Checkout',
                                    params: { lang: i18n.global.locale.value, id: ProgramsBooking.booking_id, with: 2 }
                                })
                            }
                        })
                        setTimeout(() => {
                                  
                                  window.location.reload()
                        }, 1000)
                } else {
                    loading.value = false
                    searchError.value = 'There Is No Book With This Code'
                }
            })
    }
}


watch(aboutPopup, (newVal) => {
    if (newVal) {
        document.body.style.overflow = "hidden";
    } else document.body.style.overflow = "visible";
});



onMounted(async () => {
    await axios.get(`https://seasonreal.seasonsge.com/appv1real/images` ).then((res) => {
    
         images.value=res.data
   
       });
    await axios
        .get("https://seasonreal.seasonsge.com/appv1real/slider")
        .then((data) => {
            slider.value = data.data;
        })
    await axios
        .get("https://seasonreal.seasonsge.com/appv1real/info")
        .then((data) => {
            info.value = data.data[0]
            localStorage.setItem('websiteInfo', JSON.stringify( info.value))
            document.getElementById("favicon").href = `https://seasonreal.seasonsge.com/${data.data[0].favicon}`;
        })
    setTimeout(() => {
        newPopup.value = true;
    }, 100);
});


</script>

<style lang="scss" scoped>
.bg-main-color{
    background: #FD820E;
}
.main-color{
    color: #FD820E;
}
.z-10{
    z-index: 10;
}
.z-20{
    z-index: 20;
}
.img-overlay2{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 80%;
  background: url(../assets/Images/bg1.jpg) no-repeat center;
  background-size: 100% 100%;
  opacity: 0.8;
}
.circle-shadow-o{
    //@apply w-[120px] drop-shadow-[-6px_2px_0px_rgba(0,0,0,0.25)] mx-auto h-[120px] rounded-full bg-primary flex justify-center items-center
    width: 120px;
    filter: drop-shadow(-6px 2px 0px rgba(0,0,0,0.25));
    margin-inline: auto;
    height: 120px;
    border-radius: 100%;
    background: #FD820E;
    display: flex;
    justify-content: center;
    align-items: center;
}
.circle-shadow-b{
    //@apply w-[120px] drop-shadow-[-6px_2px_0px_rgba(0,0,0,0.25)] mx-auto h-[120px] rounded-full bg-primary flex justify-center items-center
    width: 120px;
    filter: drop-shadow(-6px 2px 0px rgba(0,0,0,0.25));
    margin-inline: auto;
    height: 120px;
    border-radius: 100%;
    background: blue;
    display: flex;
    justify-content: center;
    align-items: center;
}
.contact-sec{
    padding-inline: 20px;
    padding-block: 20px;
    border-radius: 100%;
    border: 4px solid #FD820E;
}
.prim-btn {
    // @apply bg-primary text-white px-4 p-2 rounded-md hover:bg-white hover:text-primary border-2 border-primary;
    background: #FD820E;
    color: white;
    padding-inline: 16px;
    padding: 6px;
    border-radius: 6px;
    border: 2px solid #FD820E;
}
.prim-btn:hover {
    background: #fff;
    color: #FD820E;
}
.img-overlay{
    height: 300px;
//   background: url('../assets/Images/bg1.jpg') no-repeat center;
//   background-size: 100% 100%;
background: #FD820E;
}
.price-overlay{
//   @apply w-[100px] h-[100px] absolute top-[250px] rounded-full right-4 border-4 border-warning bg-white pt-2
    width: 100px;
    height: 100px;
    position: absolute;
    top: 250px;
    border-radius: 100%;
    right: 16px;
    border: solid 4px #FD820E;
    background: #fff;
    padding-top: 8px;
}
.home-page {
    .landing {
        .socials {
            right: 25px;
            bottom: 18px;

            a {
                cursor: pointer;

                i {
                    transition: 0.2s;

                    &:hover {
                        color: var(--orange-color) !important;
                    }
                }
            }
        }

        .text-box {
            &.ar {
                left: initial;
                right: 15%;
            }

            top: 50%;
            left: 15%;
            width: 550px;
            transform: translateY(-50%);
            background-color: rgba(255, 255, 255, 0.623);
            backdrop-filter: blur(5px);
            border: 2px solid var(--blue-color);

            color: var(--blue-color);

            h1 {
                font-weight: bold !important;
            }

            p {
                line-height: 1.7;
            }
        }
    }

    .about-section {
        background-color: #f5f5f5;
    }

    .reservation-section {
        .search-form {
            .search-input {
                outline: none;
                border: 1px solid gray;

                &.error {
                    border-color: #dc3545;
                }
            }
        }
    }

    .services-section {
        .box-cont {
            .box {
                box-shadow: 0 3px 15px rgba(105, 105, 105, 0.226);

                .image {
                    height: 355px;
                    overflow: hidden;

                    img {
                        object-fit: cover;
                        transition: 0.2s;

                        &:hover {
                            scale: 1.1;
                        }
                    }
                }

                .text {
                    h3 {
                        color: var(--blue-color);
                    }

                    p {
                        line-height: 1.7;
                    }

                    a {
                        font-size: 18px;
                        color: var(--orange-color);
                        transition: 0.2s;
                        width: fit-content;

                        &:hover {
                            color: #fdb89a;
                        }
                    }
                }
            }
        }
    }

    .apps-section {
        background-color: #f5f5f5;

        .apps {
            img {
                height: 70px !important;
            }
        }
    }

    .offers-section {
        // background-color: #f5f5f5;
        overflow: hidden;

        &>div {
            position: relative;
            z-index: 555;
        }

        img {
            width: 40%;
            opacity: 0.2;
            top: -50%;
            right: -5%;
            transform: rotate(25deg);
        }
    }



    @media (max-width: 991px) {
        .landing {
            .text-box {
                &.ar {
                    left: initial !important;
                    right: 50% !important;
                    transform: translate(50%, -50%) !important;
                }

                left: 50%;
                transform: translate(-50%, -50%);
            }
        }
    }

    @media (max-width: 767px) {
        .landing {
            .text-box {
                width: 90%;

                .boxes {
                    flex-wrap: wrap;
                    margin-top: 5px !important;
                }
            }

            .socials {
                right: 50% !important;
                transform: translateX(50%);
                backdrop-filter: blur(5px);
                bottom: -18px;
                background-color: rgba(0, 0, 0, 0.438);
                padding: 7px 15px 5px;
                border-radius: 5px;
            }

        }

        .reservation-section {
            form {
                flex-direction: column;

                .input-cont {
                    width: 100% !important;
                }

                button {
                    justify-content: center;
                }
            }
        }

        .apps-section {
            .apps {
                gap: 5px !important;

                img {
                    height: 50px !important;
                }
            }
        }

        .offers-section {
            img {
                width: 85%;
                top: -15%;
                right: -15%;
            }
        }
    }
}
</style>
