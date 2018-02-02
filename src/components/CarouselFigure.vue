<template>
     <div class="swiper-container">
                <div class="swiper-wrapper">
                     <div class="swiper-slide">
                        <img src="../assets/img/1.jpg">
                     </div>
                     <div class="swiper-slide">
                        <img src="../assets/img/5.png">
                     </div>
                    <div class="swiper-slide">
                        <img src="../assets/img/6.png">
                    </div>
                </div>
            <!-- Add Pagination -->
                 <div class="swiper-pagination"></div>
            <!-- Add Arrows -->
                <div class="swiper-button-next"></div>
                <div class="swiper-button-prev"></div>
            </div>
</template>

<script>
    import "swiper/dist/css/swiper.css";
    import Swiper from "swiper";    
    export default {
        name: 'CarouselFigure',
        data() {
            return {

            }
        },
         methods: {
    runSwiper() {
      var swiper = new Swiper(".swiper-container", {
        spaceBetween: 30,
        centeredSlides: true,
        autoplay: {
          delay: 2500,
          disableOnInteraction: false
        },
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        }
      });
    }
  },
  mounted() {
    this.runSwiper();
  }
    };
</script>

<style lang="scss" scoped>
.swiper-container {
  width: 100%;
  height: 30%;
}

.swiper-slide {
  height: 100%;
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
  & > img {
    display: inline-block;
    width: 100%;
    height: 100%;
  }
}

</style>