<template>
  <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="3000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="300"
      style="text-shadow: 1px 1px 2px #333"
      lazy-loading
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide
        class="img-banner"
        caption=""
        text=""
        lazy-loading
        img-src="@/assets/images/banner1.jpg"
      ></b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide
        class="img-banner"
        lazy-loading
        img-src="@/assets/images/banner2.jpg"
      >
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide
        class="img-banner"
        lazy-loading
        img-src="@/assets/images/Banner3.jpg"
      >
      </b-carousel-slide>

      <!-- Slides with img slot -->
      <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
    </b-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 3000,
      sliding: null,
    };
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    },
  },
};
</script>
