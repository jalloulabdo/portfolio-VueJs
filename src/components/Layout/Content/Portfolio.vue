<template>
        <section class="portfolio section" id="portfolio">
            <h2 class="section__title">Portfolio</h2>
            <span class="section__subtitle">Most recent work</span>
        
            <div class="portfolio_container container swiper-container">
                <div class="swiper-wrapper">
                    <!--============ PORTFOLIO 1 ==============-->
                    <div class="portfolio_content grid swiper-slide">
                        <img src="@/assets/images/Screenshot2.png" alt="" class="portfolio_img">
        
                        <div class="portfolio_data">
                            <h3 class="portfolio_title">Lux Energie Solution</h3>
                            <p class="portfolio_description">
                                Website for a company specializing in
                                heating, electricity, renewable energies
                            </p>
                        </div>
                    </div>
                    <!--============ PORTFOLIO 2 ==============-->
                    <div class="portfolio_content grid swiper-slide">
                        <img src="@/assets/images/Screenshot.png" alt="" class="portfolio_img">
        
                        <div class="portfolio_data">
                            <h3 class="portfolio_title">Yobeen Cloud</h3>
                            <p class="portfolio_description">
                                Yobeen Cloud is an application for easy, interactive, reliable and efficient management of farm
                                irrigation. and management of measured and forecast meteorological data.
                            </p>
                        </div>
                    </div>
                    <!--============ PORTFOLIO 3 ==============-->
                    <div class="portfolio_content grid swiper-slide">
                        <img src="@/assets/images/Screenshot3.png" alt="" class="portfolio_img">
        
                        <div class="portfolio_data">
                            <h3 class="portfolio_title">Table Flipping</h3>
                            <p class="portfolio_description">
                            </p>
                        </div>
                    </div>
                     <!--============ PORTFOLIO 4 ==============-->
                     <div class="portfolio_content grid swiper-slide">
                        <img src="@/assets/images/Screenshot4.png" alt="" class="portfolio_img">
        
                        <div class="portfolio_data">
                            <h3 class="portfolio_title">Yobeen Avertissement</h3>
                            <p class="portfolio_description">
                                Yobeen Avertissement is a simple to use application, which makes you connect with Towasoil device by Bluetooth, Yobeen Avertissement allows almost real monitoring of water piloting parameters in the soil through the almost immediate measurement of several depths of rooting of plants.
                            </p>
                        </div>
                    </div>
                </div>
        
                <!--Add Arrow-->
                <div class="swiper-button-next">
                </div>
                <div class="swiper-button-prev">
                </div>
                <!--Add Pagination-->
                <div class="swiper-pagination"></div>
            </div>
        </section>
</template>

<script setup>
import { onMounted } from 'vue';
import { Autoplay, Navigation, Pagination } from "swiper";
import Swiper from "swiper";
import "swiper/swiper.min.css";
Swiper.use([Autoplay, Navigation, Pagination]);
onMounted(() => {
    new Swiper('.portfolio_container', {
        observer: true,
        observeParents: true,
        parallax: true,
        slidesPerView: 1,
        loop: true,
        autoplay: true,
        simulateTouch: true,
        navigation: {
            nextEl: '.portfolio_container .swiper-button-next',
            prevEl: '.portfolio_container .swiper-button-prev',
        },
    });
})

</script>
<style>
.portfolio_data {
    max-width: 93%;
}
</style>