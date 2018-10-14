<template>
  <div>
    <h3>Demo1</h3>
    <div class="my-swiper">
      <swiper :options="swiperOption">
        <swiper-slide v-for="(img, index) in imgs" :key="index">
          <div class="item-container">
            <img :src="img">
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script>
  import { swiper, swiperSlide } from 'vue-awesome-swiper'
  export default {
    name: 'demo1',
    components: { swiper, swiperSlide },
    data () {
      return {
        swiperOption: {
          effect: 'coverflow',
          grabCursor: true,
          centeredSlides: true,
          slidesPerView: '1',
          // followFinger: false,
          coverflowEffect: {
            rotate: 50,
            stretch: 0,
            depth: 100,
            modifier: 1,
            slideShadows : true
          }
        },
        imgs: [
          require('@/assets/img/demo1/1.jpg'),
          require('@/assets/img/demo1/2.jpg'),
          require('@/assets/img/demo1/3.jpg'),
          require('@/assets/img/demo1/4.jpg'),
          require('@/assets/img/demo1/5.jpg'),
          require('@/assets/img/demo1/6.jpg'),
          require('@/assets/img/demo1/7.jpg')
        ]
      }
    }
  }
</script>

<style scoped>
  .my-swiper {
    width: 6rem;
    height: 4rem;
    margin: 0 auto;
  }
  .item-container img {
    width: 100%;
    height: 100%;
  }
</style>
