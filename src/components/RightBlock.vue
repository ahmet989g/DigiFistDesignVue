<template>  
    <section class="block-right">
        <div class="text-content mobile-hidden">
            <h3>Everyday items, we have something to suit every occasion.</h3>
            <p>At suspendisse augue lectus arcu, accumsan ut sit posuere vitae sit tincidunt semper eu proin leo gravida cursus.</p>
            <a href="javascript:;" class="linkline">Shop All Everyday Items</a>
        </div>
        <div class="product-slider-content">
            <div class="swiper product-slider">
                <swiper :breakpoints="swiperOptions.breakpoints" :navigation="swiperOptions.navigation">
                    <swiper-slide>
                        <a href="javascript:;" class="product-card">
                            <div class="product-image">
                                <img src="@/assets/images/product-1.png" alt="Product 1">
                            </div>
                            <div class="product-info">
                                <p class="product-name">Organic Skinny High Waist Raw Hem Jeans</p>
                                <div class="info-bottom">
                                    <span class="product-price">€33.95</span>
                                    <ul class="color-variants">
                                        <li class="active"><button class="btn-color blue"></button></li>
                                        <li><button class="btn-color orange"></button></li>
                                        <li><button class="btn-color purple"></button></li>
                                        <li><button class="btn-color green"></button></li>
                                    </ul>
                                </div>
                            </div>
                        </a>
                    </swiper-slide>
                    <swiper-slide>
                        <a href="javascript:;" class="product-card">
                            <div class="product-image">
                                <img src="@/assets/images/product-2.png" alt="Product 2">
                            </div>
                            <div class="product-info">
                                <p class="product-name">Organic Skinny High Waist Raw Hem Jeans</p>
                                <div class="info-bottom">
                                    <span class="product-price">€33.95</span>
                                    <ul class="color-variants">
                                        <li class="active"><button class="btn-color blue"></button></li>
                                        <li><button class="btn-color orange"></button></li>
                                        <li><button class="btn-color purple"></button></li>
                                        <li><button class="btn-color green"></button></li>
                                    </ul>
                                </div>
                            </div>
                        </a>
                    </swiper-slide>
                    <swiper-slide>
                        <a href="javascript:;" class="product-card">
                            <div class="product-image">
                                <img src="@/assets/images/product-3.png" alt="Product 3">
                            </div>
                            <div class="product-info">
                                <p class="product-name">Organic Skinny High Waist Raw Hem Jeans</p>
                                <div class="info-bottom">
                                    <span class="product-price">€33.95</span>
                                    <ul class="color-variants">
                                        <li class="active"><button class="btn-color blue"></button></li>
                                        <li><button class="btn-color orange"></button></li>
                                        <li><button class="btn-color purple"></button></li>
                                        <li><button class="btn-color green"></button></li>
                                    </ul>
                                </div>
                            </div>
                        </a>
                    </swiper-slide>
                    
                <div class="swiper-button-next" id="swiper-button-next" slot="button-next">
                    <svg width="8" height="14" viewBox="0 0 8 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M0.646447 0.646447C0.841709 0.451184 1.15829 0.451184 1.35355 0.646447L7.35355 6.64645C7.54882 6.84171 7.54882 7.15829 7.35355 7.35355L1.35355 13.3536C1.15829 13.5488 0.841709 13.5488 0.646447 13.3536C0.451184 13.1583 0.451184 12.8417 0.646447 12.6464L6.29289 7L0.646447 1.35355C0.451184 1.15829 0.451184 0.841709 0.646447 0.646447Z" fill="black"/>
                    </svg>
                </div>
                <div class="swiper-button-prev" id="swiper-button-prev" slot="button-prev">
                    <svg width="8" height="14" viewBox="0 0 8 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M0.646447 0.646447C0.841709 0.451184 1.15829 0.451184 1.35355 0.646447L7.35355 6.64645C7.54882 6.84171 7.54882 7.15829 7.35355 7.35355L1.35355 13.3536C1.15829 13.5488 0.841709 13.5488 0.646447 13.3536C0.451184 13.1583 0.451184 12.8417 0.646447 12.6464L6.29289 7L0.646447 1.35355C0.451184 1.15829 0.451184 0.841709 0.646447 0.646447Z" fill="black"/>
                    </svg>
                </div>
                </swiper>
            </div>
        </div>
    </section>
</template>
<script  lang="ts">

  import { Swiper, SwiperSlide } from 'swiper/vue';
  import SwiperCore, { Navigation } from 'swiper';
  import 'swiper/css/navigation';
  import 'swiper/css';
  SwiperCore.use([Navigation]);
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Navigation],
        swiperOptions:{
            breakpoints: {
                0: {
                    spaceBetween: 15,
                    slidesPerView:2.2,
                },
                1024: {
                    spaceBetween: 40,
                    slidesPerView:2.4,
                }
            },
            navigation: {
                nextEl: '#swiper-button-next',
                prevEl: '#swiper-button-prev',
            },
        },
      };
    },
  };
</script>
