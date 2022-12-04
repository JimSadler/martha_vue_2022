<template>
  <div id="contact-page" class="page-wrapper contact-page content-page">
    <site-hero image="/uploads/wood-3046186_1920.jpg"></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="columns">
          <div class="column">
            <h1 class="contactHead">
              Contact Us
            </h1>
          </div>
        </div>
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title contactHello">
                Hello!
              </p>
              <p class="subtitle">
                How can we help?
              </p>
              <figure class="image is-1by1">
                <opti-image
                  class="contactImg"
                  :src="require('~/assets/headshots/martha0.jpg').src"
                  :srcset="require('~/assets/headshots/martha0.jpg').srcSet"
                />
              </figure>
              <br />
            </article>
          </div>
          <div class="tile is-parent is-8">
            <article class="tile is-child box">
              <contact-form />
            </article>
          </div>
        </div>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <!-- Latest Posts -->
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import ContactForm from '~/components/ContactForm'
export default {
  head() {
    return {
      title: `Contact | ${this.$siteConfig.siteName}`
    }
  },
  components: { ContactForm }
}
</script>
<style>
@media screen and (min-width: 769px) {
  #contact-page .hero.is-medium .hero-body {
    padding-bottom: 18rem;
    padding-top: 18rem;
    margin-top: -5rem;
    text-align: right;
    padding-left: 18em;
  }
  .contactHead {
    margin-left: 55%;
    font-size: 30px;
    font-weight: 500;
  }
  img.contactImg {
    border-radius: 5px;
  }
}
button.button.contactSubmit {
  margin-left: 0%;
}
.contactHead {
  font-weight: 600;
}
.title.contactHello {
  font-weight: 400;
}
form .label {
  font-weight: 400;
}
</style>
