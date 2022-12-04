<template>
  <div>
    <div class="card">
      <div class="card-image">
        <figure class="image is-4by3">
          <img
            class="appstorebutt"
            :srcset="
              require('~/static/storeImages/ passion/horses-1078676_1920.jpg')
                .srcSet
            "
            alt
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
                :caret-animation="{
                  duration: '.6s',
                  timerFunc: 'ease-in-out'
                }"
                :slide="{
                  duration: '.9s',
                  timerFunc: 'ease'
                }"
              >
                <!-- The wrapper component for all the items -->
                <!-- eslint-disable -->
                <BulmaAccordionItem class="cardTitle">
                  <h4 slot="title">
                    <span
                      data-fsc-item-path="the-it-series"
                      data-fsc-item-display="data-fsc-item-display"
                      >The IT Series
                    </span>
                    <br />
                    <span
                      class="price"
                      data-fsc-item-path="the-it-series"
                      data-fsc-item-price="data-fsc-item-price"
                      >$15.99</span
                    >
                  </h4>
                  <p slot="content">
                    The IT Series is a powerful three DVD set of the lectures
                    Martha gives on reaching peak performance on command, the
                    non-verbal language, the Learning and Communication
                    Sequence, and much more. In demand with businesses and
                    individuals alike, this material is all about success and
                    how you can achieve presence, visibility, and much more
                    simply by adjusting the energies of the body. This is
                    material you haven't heard before anywhere else!
                  </p>
                  <a
                    slot="footer"
                    href
                    class="button is-dark"
                    data-fsc-item-path-value="the-it-series"
                    data-fsc-item-path="the-it-series"
                    data-fsc-action="Add, Checkout"
                    >Purchase</a
                  >
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
  name: 'TheITSeries',
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
