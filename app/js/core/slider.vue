<!--  -->
<template lang="html">
  <section :class="cname">
    <swiper :options="options" :not-next-click="options.notNextClick">
      <swiperSlide v-for="item in items" :key="item.href">
        <router-link :to="{name: item.href}">
          <img :src="item.src" alt="">
        </router-link>
      </swiperSlide>
      <div class="swiper-pagination" v-if="options.pagination" slot="pagination"/>
    </swiper>
  </section>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
  components: { swiper, swiperSlide },
  props: {
    options: {
      type: Object,
      default() {
        return {
          pagination: {
            el: '.swiper-pagination'
          },
          autoplay: true,
          loop: true,
          notNextClick: false
        }
      }
    },
    cname: {
      type: String,
      default: ''
    },
    items: {
      type: Array,
      default() {
        return []
      }
    }
  }
}

</script>
<style lang='scss'  >
@import "~swiper/dist/css/swiper.css";
</style>
