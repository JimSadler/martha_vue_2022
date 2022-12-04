<template>
  <!-- eslint-disable -->
  <div id="blog-page" class="page-wrapper home-page">
    <site-hero-large title="Blog Posts" subtitle image="/uploads/blog/lotus-4800281_1920.jpg"></site-hero-large>
    <main-section theme="one-column">
      <template v-slot:default>
        <!-- All Posts -->
        <posts-grid />
      </template>
      <template v-slot:sidebar>Nothing here</template>
    </main-section>
    <news-letter-form-modal />
  </div>
</template>

<script>
import { mapState } from 'vuex'
import { setPageData } from '../helper'
import NewsLetterFormModal from '~/components/NewsLetterFormModal'
import SiteHeroLarge from '~/components/SiteHeroLg'

export default {
  name: 'BlogPage',
  head() {
    return {
      title: `Blog | ${this.$siteConfig.siteName}`
    }
  },
  components: {
    NewsLetterFormModal,
    SiteHeroLarge
  },
  computed: {
    ...mapState(['title', 'subtitle', 'featureImage'])
  },
  fetch({ store, params }) {
    setPageData(store, { slug: 'home' })
  }
}
</script>

<style>
@media screen and (min-width: 769px) {
  #blog-page .hero.is-large .hero-body {
    padding-bottom: 18rem;
    padding-top: 18rem;
    text-align: right;
    padding-left: 18em;
  }
}
.home-page .under-subtitle {
  border-top: none;
}
.logo-wrapper {
  position: absolute;
  height: 82px;
  overflow: hidden;
  width: 200px;
  top: 11px;
}
.navbar a {
  transition: 0.5s ease all;
  font-weight: 500;
}
/* .navbar a:hover,
.navbar a:focus {
  color: #41b783 !important;
  text-decoration: underline;
} */
</style>
