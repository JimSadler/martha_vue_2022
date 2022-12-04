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
      <h4 slot="title">Performance Training</h4>
      <i slot="icon-open" class="material-icons">Click for Less</i>
      <i slot="icon-closed" class="material-icons">Click for More</i>
      <div slot="content">
        <p class="firstP">
          Martha Novak, LLC. is a full-service firm dedicated to improving the
          executive, management, employee, and customer experience. We teach
          companies, teams and individuals how to stand out and deliver a high
          caliber performance in today's competitive marketplace.
        </p>
        <br />
        <p>
          Most training organizations try to inspire teams. But company-wide
          growth cannot happen if the training does not inspre the individuals
          to bring all of his or her talents to the table. A company's progress
          begins with person-to-person improvement.
        </p>
        <br />
        <p>
          Most of your business’ resources are quantitative. That’s how you
          measure profit. However, your business’ most valuable resources,
          people, are qualitative. How can you accurately measure their morale,
          their enthusiasm for their work, their commitment to quality? That’s
          why businesses struggle to make worthwhile investments in their most
          important assets – their employees.
        </p>
        <br />
        <p>
          Martha Novak inspires superior results. She reaches beyond
          conventional business coaching techniques to reveal hidden blocks to
          higher achievement. She brings goals into focus and shows you the way
          to achieve them. She assesses whole-company learning and communication
          capabilities, identifies and shows you how to eliminate obstacles, and
          finally, creates an innovative, structured, customized approach that
          propels every individual forward.
        </p>
      </div>
    </BulmaAccordionItem>
  </BulmaAccordion>
</template>
<script>
export default {
  name: 'PTraining'
}
</script>
