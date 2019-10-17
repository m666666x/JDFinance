<!--  -->
<template lang="html">
  <section :class="cname">
    <swiper :options="options">
      <swiper-slide v-for="item in items" :key="item.href">
        <router-link :to="{ name:item.href }">
          <img :src="item.src" alt="">
        </router-link>
      </swiper-slide>
      <div class="swiper-pagination" v-if="options.pagination" slot="pagination"/>
    </swiper>
  </section>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
  components: {
    swiper,
    swiperSlide
  },
  props: {
    cname: {
      type: String,
      default: ''
    },
    options: {
      type: Object,
      default() {
        return {
          autoplay: true,
          loop: true,
          pagination: {
            el: '.swiper-pagination'
          },
          noteNextTick: false
        }
      }
    },
    items: {
      type: Array,
      default() {
        return { href: '', src: '' }
      }
    }
  },
  data() {
    return {
    }
  }
}

</script>
<style lang='scss' scoped>
@import "~swiper/dist/css/swiper.css";
</style>
