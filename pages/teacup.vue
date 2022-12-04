<template>
  <div id="teacup-page">
    <site-hero title="Teacup Prophecies" image="/uploads/greyGradiend.jpg">
      <h3 class="sub-page-header" role="presentation">
        Testimonial Subheader
      </h3>
    </site-hero>
    <main-section>
      <template v-slot:default>
        <Teacup></Teacup>
      </template>
      <!-- <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        <posts-grid :per-row="1" :number="2" />
      </template> -->
    </main-section>
  </div>
</template>
<script>
import Teacup from '~/components/Teacup'
export default {
  head() {
    return {
      title: `Teacup Prophecies | ${this.$siteConfig.siteName}`
    }
  },
  components: {
    Teacup
  }
}
</script>
<style scoped>
.testimonials {
  font-weight: 500;
  font-size: 18px;
}
</style>
