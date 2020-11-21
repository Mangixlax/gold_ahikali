<template>
  <div>
    <div class="main-slider">
      <div class="main-slider__show fade-in-second">
        <swiper class="slider" ref="mySwiper" :options="swiperOptions">  
            <swiper-slide class="slide"><img src="@/assets/img/slider/img1.jpg" alt=""></swiper-slide>
            <swiper-slide class="slide"><img src="@/assets/img/slider/img2.jpg" alt=""></swiper-slide>
            <swiper-slide class="slide"><img src="@/assets/img/slider/img1.jpg" alt=""></swiper-slide>
            <swiper-slide class="slide"><img src="@/assets/img/slider/img2.jpg" alt=""></swiper-slide>``
            <swiper-slide class="slide"><img src="@/assets/img/slider/img1.jpg" alt=""></swiper-slide>
            <swiper-slide class="slide"><img src="@/assets/img/slider/img2.jpg" alt=""></swiper-slide>    
        </swiper> 
      </div>
      <div class="main-slider__navigation fade-in-first">
        <h1>Подборка по преимуществам</h1>
        <p>Выберите лучшую недвижимость для себя, для своей семьи!</p>
        
        <button class="main-slider__popup-button">
          <span>Помощь в подборе</span>
        </button>

        <div class="main-slider__navigation-panel">
          <div class="prevbutton main-slider__navigation-button">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 7 10" class="erBX" data-v-f7ce66b4=""><path fill="#fff" fill-opacity=".8" d="M3.1076 5l3.1842-3.1842c.345-.345.345-.905 0-1.25s-.905-.345-1.25 0l-3.845 3.845c-.3258.3258-.3258.8533 0 1.1784l3.845 3.845c.345.345.905.345 1.25 0s.345-.905 0-1.25L3.1076 5z"></path></svg>
          </div>
          <div class="nextbutton main-slider__navigation-button">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 7 10" class="wSKq" data-v-f7ce66b4=""><path fill="#fff" d="M3.8924 5L.7082 8.1842c-.345.345-.345.905 0 1.25s.905.345 1.25 0l3.845-3.845c.3258-.3258.3258-.8533 0-1.1784L1.9582.5658c-.345-.345-.905-.345-1.25 0s-.345.905 0 1.25L3.8924 5z"></path></svg>
          </div>
        </div>
             
      </div>   
    </div>
  </div>
</template>

<script>
  export default {
    name: 'carrousel',
    data() {
      return {
        swiperOptions: {
         
          navigation: {
            nextEl: '.nextbutton',
            prevEl: '.prevbutton'
          },
            slidesPerView: "auto",
            spaceBetween: 30,
            loop: true,
            
           
        
          // Some Swiper option/callback...
        }
      }
    },

  }
</script>

<style scoped lang='scss'>

.main-slider {

  display: flex;
  min-width: 0;
  padding-right: calc(20% - 50px);
  padding-top: 32px;
  position: relative;
  
  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 425px;
    background: linear-gradient(180deg,#191f2e,#151a26);
    will-change: height;
    transition: height 0.5s cubic-bezier(0, 1, 0, 1);
    
    -webkit-animation: scale-in-ver-top 1s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
    animation: scale-in-ver-top 1s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
    @-webkit-keyframes scale-in-ver-top {
      0% {
        -webkit-transform: scaleY(0);
                transform: scaleY(0);
        -webkit-transform-origin: 100% 0%;
                transform-origin: 100% 0%;
        opacity: 1;
      }
      100% {
        -webkit-transform: scaleY(1);
                transform: scaleY(1);
        -webkit-transform-origin: 100% 0%;
                transform-origin: 100% 0%;
        opacity: 1;
      }
    }
    @keyframes scale-in-ver-top {
      0% {
        -webkit-transform: scaleY(0);
                transform: scaleY(0);
        -webkit-transform-origin: 100% 0%;
                transform-origin: 100% 0%;
        opacity: 1;
      }
      100% {
        -webkit-transform: scaleY(1);
                transform: scaleY(1);
        -webkit-transform-origin: 100% 0%;
                transform-origin: 100% 0%;
        opacity: 1;
      }
    }     
  }


  
  &__show {
    padding: 8px 30px 56px 0px;
    display: flex;
    min-width: 0;
    overflow: hidden;
    & img {
      height: 420px;
      width: 240px;
      border-radius: 10px;
    }
    
    
  }
  &__navigation {
    width: 224px;
    z-index: 50;
    margin-left: 52px;
    & h1 {
      color: #fff!important;
      display: inline-block;
      margin-top: 97px;
      margin-bottom: 24px;
      width: 224px;
      font-family: Oswald,sans-serif;
      font-style: normal;
      font-weight: 500;
      font-size: 26px;
      line-height: 34px;
      letter-spacing: .4px;
    }
    & p {
      color: hsla(0,0%,100%,.88)!important;
      font-family: Fira Sans,sans-serif;
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 26px;

    }
  }
  &__popup-button {
    margin: 35px 0 30px;
    position: relative;
    padding: 12px 36px;
    background-image: linear-gradient(266.33deg,#fed7bb,#f7c598);
    border-radius: 12px;
    
    &::before {
      content: "";
      position: absolute;
      left: 0;
      top: 0;
      right: 0;
      bottom: 0;
      background-color: #f7c598;
      opacity: 0;
    }
  }
  &__navigation-panel {
    display: flex;
  }
  &__navigation-button {
    background-color: transparent;
    width: 28px;
    height: 28px;

    
;
  }

}

 .slider {
   width: auto;
 }
 .slide {
   height: 420px;
    width: 240px;
 }

 .erBX {
   height: 9px;
 }
 .wSKq {
   width: 10px;
 }
 
 .fade-in-second {
  -webkit-animation: fade-in-second 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) 1.5s both;
            animation: fade-in-second 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) 1.5s both;
}
@-webkit-keyframes fade-in-second {
  0% {
    -webkit-transform: translateY(-50px);
            transform: translateY(-50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    opacity: 1;
  }
}
@keyframes fade-in-second {
  0% {
    -webkit-transform: translateY(-50px);
            transform: translateY(-50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    opacity: 1;
  }
}

.fade-in-first {
	-webkit-animation: fade-in-first 1.2s cubic-bezier(0.390, 0.575, 0.565, 1.000) 1.1s both;
	        animation: fade-in-first .2s cubic-bezier(0.390, 0.575, 0.565, 1.000) 1.1s both;
}

@-webkit-keyframes fade-in-first {

  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}




</style>