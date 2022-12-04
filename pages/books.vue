<template>
  <div id="books-page">
    <!-- eslint-disable -->
    <site-hero-large title="Books" image="/uploads/books/open book with pages flying away.jpg"></site-hero-large>
    <main-section theme="one-column">
      <template v-slot:default>
        <LifeYouWant></LifeYouWant>
        <Teacup></Teacup>
        <hr />
        <div class="other-posts">
          <h6 class="subtitle is-size-4">Latest Posts</h6>
          <!-- Related Posts -->
          <posts-grid :number="3" />
        </div>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">Latest Posts</h3>
        <!-- Latest Posts -->
        <posts-grid :per-row="1" :number="3" />
      </template>
    </main-section>
  </div>
</template>
<script>
import SiteHeroLarge from '~/components/SiteHeroLg'
import Teacup from '~/components/Teacup'
import LifeYouWant from '~/components/LifeYouWant.vue'

export default {
  components: {
    SiteHeroLarge,
    Teacup,
    LifeYouWant
  },
  head() {
    return {
      title: `Books | ${this.$siteConfig.siteName}`
    }
  }
}
</script>
<style>
@media screen and (min-width: 769px) {
  #books-page .hero.is-large .hero-body {
    padding-bottom: 18rem;
    padding-top: 18rem;
    text-align: right;
    padding-left: 18em;
  }
  .hero-theme-dark .title,
  .hero-theme-dark .subtitle,
  .hero-theme-dark .under-subtitle,
  .hero-theme-dark .under-subtitle strong {
    color: white;
  }
  ul.teacupPurchasButtons {
    text-align: center;
    margin-left: 0%;
    margin-top: 2%;
  }
}
.teacupQuoteList {
  list-style: inherit;
  padding: 2% 2%;
}
.book_buttons {
  padding-top: 5%;
  display: inline-block;
}
.book_buttons button.animated-button {
  margin-right: 10px;
  display: inline-block;
  margin-left: 0%;
}

@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  #books-page .hero-theme-dark .title,
  #books-page .hero-theme-dark .subtitle,
  #books-page .hero-theme-dark .under-subtitle,
  #books-page .hero-theme-dark .under-subtitle strong {
    color: white;
  }
}
</style>
