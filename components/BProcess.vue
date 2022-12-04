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

    <BulmaAccordionItem class role="button" tabindex="0">
      <h4 slot="title" role="button" tabindex="0">The Infinite Insight Process</h4>
      <i slot="icon-open" class="material-icons">Click for Less</i>
      <i slot="icon-closed" class="material-icons">Click for More</i>
      <div slot="content">
        <p>
          With her trademark evaluation, Martha Novak assesses the individual's
          learning and communication process and provides companies with graphs
          of the results. We interpret the charts for you, teach you how to
          interpret them for future use, and present the information to the
          company according to your needs – suggesting the best team and/or job
          restructuring to management, running team comparisons, assessing
          individual performance, predicting conflicts, and presenting
          solutions. Our Learning and Communication Sequence (LCS) Assessments
          are an invaluable tool when hiring, merging, acquiring or downsizing.
        </p>
        <br />
        <h3 class="bprocessHeading">II.Interview and Discovery</h3>

        <p>
          Martha Novak,LLC. conducts extensive research before we begin. We
          interveiw, privately and confidentially, anyone the company
          designates, including but not limited to its executive officers. We
          discover strenghts and challenges, and devise efficient strategies to
          address each.
        </p>
        <br />
        <h3 class="bprocessHeading">III. PPI Training and Systematic Access</h3>

        <p>
          Peak Performance Improvement (PPI) Training is a methodic approach,
          tailor-made to your organization and its needs. Employee by employee,
          we show your company how to work at higher levels of performance.
          Systematic Access is the hands on coaching process for the executives,
          teams and individuals within your organization. We take the quickest
          route to help break old patterns that no longer serve your
          organization and its goals, and train people to adopt more powerful
          behaviors. You’ll see performance improve markedly, and immediately.
        </p>
        <br />
        <h3 class="bprocessHeading">IV. Planning and Evaluation</h3>

        <p>
          After implementation of Infinite Insight, we sit down with you and
          determine how far you’ve come and where you want to go next. At this
          time, we may conduct more interviews, survey your new image, or design
          an itinerary that will guide you further on your journey, helping you
          choose and arrive at the next, more ambitious destination.
        </p>
      </div>
    </BulmaAccordionItem>
  </BulmaAccordion>
</template>
<script>
export default {
  name: 'BProcess'
}
</script>
