<template>
  <BulmaAccordion
    dropdown
    icon="custom"
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
    <!-- eslint-disable -->

    <BulmaAccordionItem class>
      <h4 slot="title">The Infinite Insight Advantage</h4>
      <i slot="icon-open" class="material-icons">Click for Less</i>
      <i slot="icon-closed" class="material-icons">Click for More</i>
      <div slot="content">
        <p class="firstP">
          What is the difference between a good coach and a great one? Being a
          great coach requires out-of-the-box thinking, exceptional insight and
          the ability to assess with neutrality. A great coach is an expert
          communicator who links you to your potential. It’s easy to detect bad
          coaches: their methods don’t lead to the power of your potential.
          Instead they ask you to imitate their potential.
        </p>
        <br />
        <p>
          How does having a great coach benefit you? Growth is an adventure. By
          helping you identify and overcome personal obstacles, a great coach
          does more than teach you to imitate behaviors that work for most
          people. A great coach facilitates your evolution, ensuring that the
          training is effective and enduring.
        </p>
      </div>
    </BulmaAccordionItem>
  </BulmaAccordion>
</template>
<script>
export default {
  name: 'BAdvantage'
}
</script>
<style scoped>
.features.now {
  padding-top: 3% !important;
}
</style>
