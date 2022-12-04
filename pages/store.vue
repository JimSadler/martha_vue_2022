<template>
  <div id="store-page">
    <site-hero-large
      title="Store"
      subtitle="Video and Audio Merchandise "
      image="/uploads/frog-540812_1920.jpg"
    ></site-hero-large>
    <main-section>
      <template v-slot:default>
        <div class="columns">
          <div class="column is-full">
            <h2 class="level2">Video Downloads</h2>
            <hr />
          </div>
        </div>
        <div class="columns firstColumn">
          <div class="column">
            <Passion></Passion>
          </div>
          <div class="column">
            <Flow></Flow>
          </div>
          <div class="column">
            <Intimacy></Intimacy>
          </div>
          <div class="column">
            <TrueFreedom></TrueFreedom>
          </div>
          <div class="column">
            <TheITSeries />
          </div>
        </div>
        <div class="columns">
          <div class="column is-full">
            <h2 class="level2">Audio Downloads</h2>
            <hr />
          </div>
        </div>
        <div class="columns firstColumn">
          <div class="column">
            <JoyofFear></JoyofFear>
          </div>
          <div class="column">
            <Relationships101></Relationships101>
          </div>
          <div class="column">
            <BetrayingtheChild></BetrayingtheChild>
          </div>
          <div class="column">
            <PrayersforRealLife></PrayersforRealLife>
          </div>
        </div>
        <!-- <div class="columns">
          <div class="column is-full">
            <h2 class="level2">Courses</h2>
            <hr />
          </div>
        </div>-->
        <!-- <div class="columns firstColumn">
          <div class="column is-one-quarter">
            <Relationships101Course></Relationships101Course>
          </div>
          <div class="column is-one-quarter">
            <JoyofFearCourse></JoyofFearCourse>
          </div>
        </div>-->
      </template>
    </main-section>
  </div>
</template>
<script>
import SiteHeroLarge from '~/components/SiteHeroLg'
import Passion from '~/components/cards/Passion.vue'
import Flow from '~/components/cards/Flow.vue'
import Intimacy from '~/components/cards/Intimacy.vue'
import TrueFreedom from '~/components/cards/TrueFreedom.vue'
import BetrayingtheChild from '~/components/cards/BetrayingtheChild.vue'
import PrayersforRealLife from '~/components/cards/PrayersforRealLife.vue'
import JoyofFear from '~/components/cards/JoyofFear.vue'
import Relationships101 from '~/components/cards/Relationships101.vue'
import TheITSeries from '~/components/cards/TheITSeries.vue'
// import Relationships101Course from '~/components/cards/courses/Relationships101Course.vue'
export default {
  components: {
    SiteHeroLarge,
    Passion,
    Flow,
    Intimacy,
    TrueFreedom,
    BetrayingtheChild,
    PrayersforRealLife,
    JoyofFear,
    TheITSeries,
    Relationships101
    // Relationships101Course
  },
  head() {
    return {
      title: `Store | ${this.$siteConfig.siteName}`
    }
  }
}
</script>
<style>
@media screen and (min-width: 769px) {
  #store-page .hero.is-large .hero-body {
    padding-bottom: 18rem;
    padding-top: 18rem;
    margin-left: 70%;
    padding-left: 0em;
  }
  iframe#fsc-popup-frame {
    min-height: 100%;
  }
}
.card-header {
  transition: 0.5s ease all;
}
.card-header:hover {
  background-color: #e5e3e3;
}
.card-header-title {
  padding: 1.75rem 1rem !important;
}
h2.level2 {
  font-size: 22px;
  font-weight: 500;
  text-align: center;
  padding-top: 5%;
}
.accordion .card-header-title {
  display: inline-block !important;
}
.accordion p.card-header-icon {
  display: inline-block !important;
}
</style>
