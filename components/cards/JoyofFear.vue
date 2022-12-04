<template>
  <div>
    <div class="card">
      <div class="card-image">
        <figure class="image is-4by3">
          <img
            class="appstorebutt"
            :srcset="
              require('~/static/storeImages/ passion/dog-2723082_1920.jpg')
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
                icon="custom"
                :caret-animation="{
                  duration: '.3s',
                  timerFunc: 'ease-in-out'
                }"
                :slide="{
                  duration: '.3s',
                  timerFunc: 'ease'
                }"
              >
                <!-- The wrapper component for all the items -->
                <BulmaAccordionItem class="cardTitle">
                  <h4 slot="title">
                    <span
                      data-fsc-item-path="JoyFearWorry"
                      data-fsc-item-display="data-fsc-item-display"
                    >
                      The Joy of Fear & Worry
                    </span>
                    <br />
                    <span
                      class="price"
                      data-fsc-item-path="JoyFearWorry"
                      data-fsc-item-price="data-fsc-item-price"
                    >
                      $2.99
                    </span>
                  </h4>
                  <i slot="icon-closed" class="fas fa-chevron-down"></i>
                  <i slot="icon-open" class="fas fa-chevron-up"></i>
                  <p slot="content">
                    Exploring the purposes of fear and worry in our daily lives,
                    we see that these things are part of the Dynamic Whole and
                    essential to our growth and well-being. This recording
                    exposes fear and worry for what they are and takes the sting
                    out of them, giving you a new perspective on old conditions
                    that will move out of your life as Consciousness awakens.
                  </p>
                  <a
                    slot="footer"
                    href
                    class="button is-dark"
                    data-fsc-item-path="JoyFearWorry"
                    data-fsc-item-path-value="JoyFearWorry"
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
import { BulmaAccordion, BulmaAccordionItem } from 'vue-bulma-accordion'
export default {
  name: 'JoyofFear',
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
.card-header {
  background-color: transparent;
  -webkit-box-align: stretch;
  align-items: stretch;
  box-shadow: 0 0.125em 0.25em rgba(10, 10, 10, 0.1);
  display: -webkit-box;
  display: flex;
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
