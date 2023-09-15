<template>
  <div class="carousel center">
    <HeaderComp />
    <div class="details center">
      <h2 class="details__header">{{ header }}</h2>
      <p class="details__text">{{ text }}</p>
    </div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="../components/img/carousel.png"
            alt="слот изображения"
          />
        </template>
      </b-carousel-slide>
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="../components/img/carousel.png"
            alt="слот изображения"
          />
        </template> </b-carousel-slide
      ><b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="../components/img/carousel.png"
            alt="слот изображения"
          />
        </template>
      </b-carousel-slide>
    </b-carousel>
    <FooterComp />
  </div>
</template>

<script>
import { mapState } from "vuex";
import FooterComp from "@/components/FooterComp.vue";
import HeaderComp from "@/components/HeaderComp.vue";
export default {
  name: "ProjectDetails",
  data() {
    return { slide: 0, sliding: null };
  },
  mounted() {},
  methods: {
    onSlideStart() {
      this.sliding = true;
    },
    onSlideEnd() {
      this.sliding = false;
    },
  },
  computed: {
    ...mapState(["header", "text"]),
  },
  components: { HeaderComp, FooterComp },
};
</script>

<style lang="scss" scoped>
.details {
  &__header {
    color: #292f36;
    font-family: DM Serif Display;
    font-size: 50px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%; 
    letter-spacing: 1px;
  }
  &__text {
    color: #4d5053;
    font-family: Jost;
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%; 
    letter-spacing: 0.22px;
  }
}
</style>
