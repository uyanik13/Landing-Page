<template>
  <div class="container mx-auto sm:px-0 lg:px-24 h-16 mb-2 grid justify-between items-center ">
            <carousel :settings="settings" :breakpoints="breakpoints" class="mt-12 hidden sm:block md:block lg:flex"  >
              <slide  v-for="item in stories" :key="item.id" class="block" :data-index="item.id" :data-name="`slide`+item.id">
                  <img :src="item.img" class="w-20 ml-4 rounded-full border-default border-transparent hover:border-primary">
                  <span class="text-xs mt-2 ">{{item.title}}</span>
              </slide>
                <template #addons>
                <navigation />
              </template>
            </carousel>

          <div id="content" class="flex">
              <div class="lg:mt-8 lg:w-full mb-2 flex justify-between items-start   ">
                <div class="shadow-lg block lg:mr-2 ">
                    <div v-for="item in banners" :key="item.id" 
                          @mouseover="showBannerRightText(`${item.id}`)"
                          @mouseleave="hideBannerRightText(`${item.id}`)" 
                          class="text-white bg-black transition duration-500 ease-in-out hover:bg-primary mb-5">
                        <a href="#">
                          <span >
                            <img :src="item.img"
                            class="transition duration-500 ease-in-out transform  hover:-translate-y-1">
                          </span>
                          <summary class="flex items-center justify-between px-2 py-1 text-sm">
                                <span>
                                  {{item.title}}
                                </span> 
                                <span  v-show="item.closedTime" :ref="`banner-right-text-closed-time-${item.id}`" class="">
                                    <countdown :date="item.closedTime"></countdown>
                                </span> 
                                <span  :ref="`banner-right-text-${item.id}`" class="hidden">
                                  Alışverişe Başla
                                  <font-awesome-icon :icon="['fas', 'angle-right']" class="ml-2 text-4"  />
                                </span> 
                          </summary>
                      </a>
                    </div>
                </div>
              </div>

              <div class="w-4/12 mt-8 hidden sm:block md:block lg:block" >
                  <carousel item-to-show="1" class="mb-2" >
                      <slide  v-for="item in squarBanners" :key="item.id" class="" :data-index="item.id" :data-name="`slide`+item.id">
                        <img :src="squarBanners[0].img" class="w-64 ">
                      </slide>
                      <template #addons>
                        <navigation />
                      </template>
                  </carousel>
                  <carousel item-to-show="1" class="mb-2" >
                      <slide  v-for="item in squarBanners" :key="item.id" class="" :data-index="item.id" :data-name="`slide`+item.id">
                        <img :src="squarBanners[0].img" class="w-64 ">
                      </slide>
                      <template #addons>
                        <navigation />
                      </template>
                  </carousel>
                  <carousel item-to-show="1"  class="mb-2" >
                      <slide  v-for="item in squarBanners" :key="item.id" class="" :data-index="item.id" :data-name="`slide`+item.id">
                        <img :src="squarBanners[0].img" class="w-64 ">
                      </slide>
                      <template #addons>
                        <navigation />
                      </template>
                  </carousel>  
              </div>
          </div>
          
  </div>
</template>

<script>

import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Navigation } from 'vue3-carousel';
import  countdown from '../components/custom/countdown';


export default {
  name: 'Home',
  components: {
    Carousel,
    Slide,
    Navigation,
    countdown

    
  },
  computed: {
    
  },
  methods : {
    showBannerRightText (refID){
       this.$refs[`banner-right-text-${refID}`].classList.remove('hidden')
       if (this.$refs[`banner-right-text-closed-time-${refID}`]){
          this.$refs[`banner-right-text-closed-time-${refID}`].classList.add('hidden')
       }
      },
    hideBannerRightText (refID){
       this.$refs[`banner-right-text-${refID}`].classList.add('hidden')
       if (this.$refs[`banner-right-text-closed-time-${refID}`]){
          this.$refs[`banner-right-text-closed-time-${refID}`].classList.remove('hidden')
       }
      },
      
  },
data () {
    return {
        settings: {
          itemsToShow: 9,
          snapAlign: "center"
       },
       breakpoints: {
        // 700px and up
        700: {
          itemsToShow: 3.5,
          snapAlign: "center"
        },
        // 1024 and up
        1024: {
          itemsToShow: 10.5,
          snapAlign: "start"
        }
      },

      stories : [
            {
              id:1,
              img:'https://cdn.dsmcdn.com/assets/t/y/creative/ds/Automation/Widget/2019/12/16/seninicin.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Sana Ozel',
            },
            {
              id:2,
              img:'https://cdn.dsmcdn.com/assets/t/y/creative/ds/Automation/Widget/2019/12/16/coksatanlar.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Sende Al'
            },
            {
              id:3,
              img:'https://cdn.dsmcdn.com/marketing/datascience/automation/2020/12/30/EglenceWeb_202012301831.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Oyun & Eglence'
            },
            {
              id:4,
              img:'https://cdn.dsmcdn.com/assets/t/y/Creative/ds/Automation/SquareLogosIteration3/trendyolmilla__brand__40.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Oyun & Eglence'
            },
            {
              id:5,
              img:'https://cdn.dsmcdn.com/assets/t/y/Creative/ds/Automation/SquareLogosIteration3/koton__brand__842.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Oyun & Eglence'
            },
            {
              id:6,
              img:'https://cdn.dsmcdn.com/Assets/t/y/Creative/ds/Automation/Widget/2020/5/12/Logopull_202005120822.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Oyun & Eglence'
            },
            {
              id:7,
              img:'https://cdn.dsmcdn.com/assets/t/y/Creative/ds/Automation/SquareLogosIteration3/trend-alacati-stili__brand__13025.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Oyun & Eglence'
            },
            {
              id:8,
              img:'https://cdn.dsmcdn.com/assets/t/y/Creative/ds/Automation/SquareLogosIteration3/trendyolman__brand__15508.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Oyun & Eglence'
            },
            {
              id:9,
              img:'https://cdn.dsmcdn.com/assets/t/y/Creative/ds/Automation/SquareLogosIteration3/cool--sexy__brand__564.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Oyun & Eglence'
            },
            {
              id:10,
              img:'https://cdn.dsmcdn.com/assets/t/y/Creative/ds/Automation/SquareLogosIteration3/pierre-cardin__brand__121.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Oyun & Eglence'
            },
            {
              id:11,
              img:'https://cdn.dsmcdn.com/assets/t/y/Creative/ds/Automation/SquareLogosIteration3/pierre-cardin__brand__121.png',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Oyun & Eglence'
            },
            {
              id:12,
              img:'https://cdn.dsmcdn.com/marketing/datascience/automation/BrandBoutique/2020/7/13/olalook.jpg',
              slug:'https://www.trendyol.com/sanaozel/1?versionKey=mixedMerchandisedProducts',
              title : 'Oyun & Eglence'
            },

      ],

      banners : [
        {
          id:1,
          title:'TRENDYOLMİLLA & TRENDYOL MAN',
          img:'https://cdn.dsmcdn.com/marketing/datascience/automation/2021/1/7/Trendyolmillatrendyolman_Kadin_Webbig_202101071216.jpg',
          closedTime: null,
        },
        {
          id:2,
          title:'TRENDYOLMİLLA & TRENDYOL MAN - En İyilerde Fırsatlar',
          img:'https://cdn.dsmcdn.com/ty45/campaign/banners/original/548537/6976bbec09_0_new.jpg',
          closedTime: '2021-01-07 19:15:00',
        },
        {
          id:3,
          title:'LC Waikiki- Yetişkin & Çocuk & Ev',
          img:'https://cdn.dsmcdn.com/ty45/campaign/banners/original/533989/6c5693a9c5_1_new.jpg',
          closedTime: null,
        },
      ],
      squarBanners : [
        {
          id:1,
          img:'assets/img/product-1.png',
        },
        {
          id:2,
          img:'assets/img/product-2.png',
  
        },
        
      ]
   
     }
  },
}
</script>
<style >
    .carousel__icon {
      background-color: transparent;
      color: black;
    }
    .carousel__prev, .carousel__next{
      background-color: transparent;
    }
</style>