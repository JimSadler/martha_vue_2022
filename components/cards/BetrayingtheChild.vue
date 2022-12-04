<template>
  <div>
    <div class="card">
      <div class="card-image">
        <figure class="image is-4by3">
          <img
            class="appstorebutt"
            :srcset="
              require('~/static/storeImages/ passion/child-817373_1920.jpg')
                .srcSet
            "
            alt=""
          />
        </figure>
      </div>
      <div class="card-content">
        <div class="media">
          <div class="media-content">
            <client-only>
              <BulmaAccordion
                dropdown
                icon="plus-minus"
                :caretAnimation="{
                  duration: '.6s',
                  timerFunc: 'ease-in-out'
                }"
                :slide="{
                  duration: '.9s',
                  timerFunc: 'ease'
                }"
              >
                <!-- The wrapper component for all the items -->
                <BulmaAccordionItem class="cardTitle">
                  <h4 slot="title">
                    <span
                      data-fsc-item-path="betraying-the-inner-child-again-and-again"
                      data-fsc-item-display="data-fsc-item-display"
                      >Betraying the Child Again & Again
                    </span>

                    <span
                      class="price"
                      data-fsc-item-path="betraying-the-inner-child-again-and-again"
                      data-fsc-item-price="data-fsc-item-price"
                    >
                      $2.99</span
                    >
                  </h4>
                  <p slot="content">
                    Each of you carries a virtual child within you to help you
                    heal from the old wounds of the past. Enlisting the inner
                    child in your healing is a powerful tool in order for you
                    become a Full and Vibrant Being in the Now. In this
                    recording, learn all about how to use the inner child - for
                    more insights, to map your progress of healing and to become
                    One with yourself - which is the first step to becoming One
                    with all of Life.
                  </p>
                  <a
                    slot="footer"
                    href
                    class="button is-dark"
                    data-fsc-item-path="betraying-the-inner-child-again-and-again"
                    data-fsc-item-path-value="betraying-the-inner-child-again-and-again"
                    data-fsc-action="Add, Checkout"
                  >
                    Purchase
                  </a>
                </BulmaAccordionItem>
              </BulmaAccordion>
            </client-only>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// import { BulmaAccordion, BulmaAccordionItem } from 'vue-bulma-accordion'
export default {
  name: 'BetrayingtheChild',
  data() {
    return {}
  }
}
</script>
<style scoped>
.card-header-title h4 {
  font-size: 16px;
  font-weight: 600;
}
.button.is-dark {
  margin: 5% auto;
}
.card-content {
  padding: 0;
}
.accordion .card-content {
  padding: 3%;
}
.cardTitle.card .card-header-title {
  padding: 1.75rem 1rem;
}
.card-header {
  background-color: transparent;
  -webkit-box-align: stretch;
  align-items: stretch;
  box-shadow: 0 0.125em 0.25em rgba(10, 10, 10, 0.1);
  display: -webkit-box;
  display: flex;
}
.card-header-title {
  -webkit-box-align: center;
  align-items: center;
  color: #363636;
  display: -webkit-box;
  display: flex;
  -webkit-box-flex: 1;
  flex-grow: 1;
  font-weight: 700;
  padding: 0.75rem 1rem;
}
.card-header-icon {
  -webkit-box-align: center;
  align-items: center;
  cursor: pointer;
  display: -webkit-box;
  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  padding: 0.75rem 1rem;
}
</style>
