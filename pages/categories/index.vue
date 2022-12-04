<template>
  <div id="categories-page" class="page-wrapper categories-page">
    <site-hero title="Categories" image="/uploads/blossom-4933846_1920.jpg" />
    <main-section theme="one-column">
      <categories-grid />
    </main-section>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: `Categories | ${this.$siteConfig.siteName}`
    }
  }
}
</script>
<style>
@media screen and (min-width: 769px) {
  #categories-page .hero.is-medium .hero-body {
    padding-bottom: 18rem;
    padding-top: 18rem;
    text-align: right;
    padding-left: 18em;
  }
}
</style>
