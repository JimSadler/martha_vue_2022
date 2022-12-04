<template>
  <BulmaAccordion
    dropdown
    icon="custom"
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
    <BulmaAccordionItem class role="button" tabindex="0">
      <h4 slot="title" role="button" tabindex="0">The Infinite Insight for Business</h4>
      <i slot="icon-open" class="material-icons">Click for Less</i>
      <i slot="icon-closed" class="material-icons">Click for More</i>
      <div slot="content">
        <p>
          The Process defines a system of peak performance which allows
          people to generate high energy on command without anxiety.
          this method of achieving peak performance energy far exceeds
          generic business-seminar-style peak performance training. It
          renders visibility, bestows the dynamic of all great leadership,
          and opens the door to consistantly high levels of accomplishment
          through peak perfromance behaviors.
        </p>
        <br />
        <p>
          Infinite Insight delievers powerful, life-changing perpectives on
          peak performance, communication, teamwork, sales, the power of
          perception, conflict management and resolution, and the inherent
          power of non-verbal language. As a result, employees learn to
          achieve consistantly high levels of performance on command.
        </p>
        <!-- eslint-enable -->
      </div>
    </BulmaAccordionItem>
  </BulmaAccordion>
</template>
<script>
export default {
  name: 'BProcessBus'
}
</script>
