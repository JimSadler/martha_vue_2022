<template>
  <div>
    <div class="card">
      <div class="card-image">
        <figure class="image is-4by3">
          <img
            class="appstorebutt"
            :srcset="
              require('~/static/storeImages/ passion/dove-2516641_1920.jpg')
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
                  duration: '.3s',
                  timerFunc: 'ease-in-out'
                }"
                :slide="{
                  duration: '.03s',
                  timerFunc: 'ease-in-out'
                }"
              >
                <!-- The wrapper component for all the items -->
                <!-- eslint-disable -->
                <BulmaAccordionItem class="cardTitle">
                  <h4 slot="title">
                    <span
                      data-fsc-item-path="true-freedom"
                      data-fsc-item-display="data-fsc-item-display"
                      >True Freedom</span
                    >
                    <br />
                    <span
                      class="price"
                      data-fsc-item-path="true-freedom"
                      data-fsc-item-price="data-fsc-item-price"
                      >$9.99</span
                    >
                  </h4>
                  <p slot="content">
                    True freedom is freedom from self imposed tyranny.
                  </p>
                  <a
                    slot="footer"
                    href
                    class="button is-dark"
                    data-fsc-item-path-value="true-freedom"
                    data-fsc-item-path="true-freedom"
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
import { BulmaAccordion, BulmaAccordionItem } from 'vue-bulma-accordion'
export default {
  name: 'TrueFreedom',
  components: { BulmaAccordion, BulmaAccordionItem },
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
