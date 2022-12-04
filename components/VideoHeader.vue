<template>
  <client-only>
    <div class="parallax-container">
      <div class="aside-overlay">
        <div class="container parallax-title">
          <div class="row text-center">
            <div class="col-lg-12">
              <!-- <h2>Your Website, Your Way</h2> -->
            </div>
          </div>
        </div>
      </div>
      <Parallax :speed-factor="0.3" breakpoint="(min-width: 50px)">
        <video
          autoplay
          muted
          loop
          id="bgvideo"
          is-fixed="true"
          breakpoint="(min-width: 768px)"
        >
          <source :src="selectedVideo" :type="videoType" />
        </video>
      </Parallax>
    </div>
  </client-only>
</template>
<script>
import Parallax from 'vue-parallaxy'
export default {
  components: {
    Parallax
  },
  name: 'VideoHeader',
  data() {
    return {
      videoType: 'video/mp4',
      slide: 0,
      sliding: null,
      videos: [require('~/assets/videos/lakeDockMountain.mp4')],
      selectedVideo: ''
    }
  },
  created() {
    const idx = Math.floor(Math.random() * this.videos.length)
    this.selectedVideo = this.videos[idx]
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    }
  }
}
</script>

<style scoped>
.bg-parallax-dark {
  min-height: 65vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: #fff;
}
.cta_button1 {
  width: 20%;
  margin-left: 41%;
  z-index: 2000;
  text-align: center;
}

img#logoCta2,
img#logoCta3 {
  z-index: 1000;
  margin: auto;
  width: 28%;
}
.CTA-logo1 {
  margin-right: 0%;
  margin-left: 0%;
}
.Masthead__image.is-parallax {
  left: 0;
  position: inherit;
  will-change: transform;
  right: 0;
  top: 0;
}
.parallax-container[data-v-7da0ed7c] {
  position: relative;
  width: 120vh;
}
@media screen and (min-width: 768px) {
  .Masthead {
    min-height: 114vh;
  }
}
.parallax-container {
  position: absolute !important;
  width: 211vh !important;
}

video#bgvideo {
  width: 100%;
}

.parallax-title {
  position: relative;
  top: 30%;
  left: 0;
  right: 0;
  padding: 20px;
  /* background: rgba(0, 0, 0, 0.4); */
  color: white;
  text-align: center;
  width: 100%;
}

a {
  font-family: 'NoirPro_light', Fallback, sans-serif;
}
@media (max-width: 768px) {
  .parallax-container {
    display: none;
  }
}
</style>
