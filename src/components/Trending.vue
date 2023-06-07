<script>
import data from "../data.json";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/pagination";
import { Pagination } from "swiper";

export default {
  name: "Trending",
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      datas: data,
    };
  },
  computed: {
    filterTrending() {
      return this.datas.filter((movie) => movie.isTrending);
    },
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
  mounted() {
    console.log(data);
  },
};
</script>
<template>
  <swiper
    :slidePerView="7"
    :spaceBetween="30"
    :pagination="{
      clickable: 'false',
    }"
    :modules="modules"
    class="container">
    <swiper-slide
      v-for="movie in filterTrending"
      class="trending_container"
      v-bind:style="{
        backgroundImage: `url(${movie.thumbnail.trending.small})`,
        backgroundRepeat: 'no-repeat',
      }">
      <div class="details">
        <p>{{ movie.year }}</p>
        <p>
          <img
            v-if="movie.category === 'Movie'"
            src="../../public/assets/icon-nav-movies.svg"
            alt="movie"
            width="15" />
          <img
            v-else
            src="../../public/assets/icon-nav-tv-series.svg"
            alt="series"
            width="15" />
          {{ movie.category }}
        </p>

        <p>{{ movie.rating }}</p>
      </div>
      <h4>{{ movie.title }}</h4>
    </swiper-slide>
  </swiper>
</template>

<style scoped>
.container {
  /* display: flex; */
  /* margin-top: 20px; */
}
.trending_container {
  width: 200px;
  height: 150px;
  border-radius: 10px;
}
.details {
  display: flex;
  padding-top: 100px;
  gap: 10px;
}
</style>
