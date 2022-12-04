<template>
  <div>
    <div class="card">
      <div class="card-image">
        <div class="image is-4by3">
          <img
            src="~/assets/uploads/tulips-2166508_1920.jpg"
            alt="Placeholder image"
          />
        </div>
      </div>
      <div class="card-content">
        <div class="media">
          <div class="media-content">
            <client-only placeholder="Loading...">
              <BulmaAccordion
                dropdown
                icon="plus-minus"
                :caret-animation="{
                  duration: '0s',
                  timerFunc: 'ease-in-out'
                }"
                :slide="{
                  duration: '0s',
                  timerFunc: 'ease'
                }"
              >
                <!-- The wrapper component for all the items -->
                <BulmaAccordionItem class="cardTitle">
                  <h4 slot="title">
                    <span
                      data-fsc-item-path="passion"
                      data-fsc-item-display="passion"
                    >
                      Passion
                    </span>
                    <br />
                    <span
                      class="price"
                      data-fsc-item-path="passion"
                      data-fsc-item-price="data-fsc-item-price"
                    >
                      $9.99
                    </span>
                  </h4>
                  <p slot="content">
                    Passion, what it is, how you go about enjoying it, and how
                    to get more of it. We are supposed to be passionate about
                    our lives, our families, our friends, and what we do in the
                    world.
                  </p>
                  <a
                    slot="footer"
                    href
                    class="button is-dark"
                    data-fsc-item-path-value="passion"
                    data-fsc-item-path="passion"
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
  name: 'Passion',
  data() {
    return {
      featuresOpen: false
    }
  },
  methods: {
    toggleFeatures() {
      this.featuresOpen = !this.featuresOpen
    }
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
