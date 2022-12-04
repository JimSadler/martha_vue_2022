<template>
  <!-- eslint-disable -->
  <div id="infinite-page">
    <site-hero
      title="What We Do"
      image="/uploads/sunset-1373171_1920.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="columns">
          <div class="column is-full">
            <!-- <h2
              class="level2"
              style="margin-bottom: .5rem;"
            >Infinite Insight is the correction of false assumptions.</h2>-->

            <p class="infiniteIntro">
              Infinite Insight is the correction of false assumptions. We spend
              all our lives trying to be loved. But our journey is not about
              being loved,
              <br />it is about Being Love. This is what our company
              facilitates. We invite you to listen to our audio clips, hear
              Martha Novak in person, and participate in her group healing
              sessions that she does in her hometown Atlanta and in cities
              around the world.
            </p>
            <br />
            <p>
              Martha is the real thing, a true motivator and inspirational
              leader as well as a great teacher who cares deeply about people
              and about their journey into Wholeness. Her abilities are
              astounding and she continues to offer deep and life-altering
              insights the likes of which you will never hear anywhere else.
            </p>
            <br />
            <p>
              We invite you to work with Martha and the people she has trained.
              All go through a long, rigorous process to be certified. This
              group of facilitators are top-notch professionals who have worked
              with Martha and with Infinite Insight for years.
            </p>
          </div>
        </div>
        <div class="columns">
          <div class="column is-full now now1 now3">
            <BAdvantage></BAdvantage>
          </div>
        </div>
        <div class="columns">
          <div class="column is-full">
            <BProcessBus></BProcessBus>
          </div>
        </div>
        <div class="columns">
          <div class="column is-full">
            <PTraining></PTraining>
          </div>
        </div>
        <div class="columns">
          <div class="column is-full">
            <BProcess></BProcess>
          </div>
        </div>
        <div class="columns">
          <div class="column is-full">
            <LCS></LCS>
          </div>
        </div>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">Latest Posts</h3>
        <!-- Latest Posts -->
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import BAdvantage from '~/components/BAdvantage'
import BProcessBus from '~/components/BProcessBus'
import PTraining from '~/components/PTraining'
import BProcess from '~/components/BProcess'
import LCS from '~/components/LCS'
export default {
  components: {
    BAdvantage,
    PTraining,
    BProcessBus,
    BProcess,
    LCS
  },
  head() {
    return {
      title: `Infinite Insight | ${this.$siteConfig.siteName}`
    }
  }
}
</script>
<style>
h2.level2 {
  font-size: 22px;
  font-weight: 500;
  text-align: center;
  padding-top: 5%;
}
.button.is-fullwidth {
  margin-bottom: 3%;
}
h3.bprocessHeading {
  font-size: 17px;
  font-weight: 500;
  padding-bottom: 1%;
}
hr {
  background-color: whitesmoke;
  border: none;
  display: block;
  height: 2px;
  margin: 0.5rem 0 1.5rem;
}
#infinite-page p.card-header-title {
  font-size: 20px;
  text-align: center;
}
#infinite-page .under-subtitle {
  display: inline-block;
  font-size: 1rem;
  border-top: none !important;
  padding-top: 5px;
}
#infinite-page .icon {
  width: 6.5rem !important;
}
i.material-icons {
  margin-right: 0 !important;
  padding-top: 2.5rem;
}
@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  .card-header-title {
    padding: 0.25rem;
  }
  .plus-minus[data-v-6b0c21ae] {
    position: relative;
    display: block;
    width: 80%;
    height: 80%;
  }
}
i.material-icons {
  margin-right: 50px;
}
</style>
