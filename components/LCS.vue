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

    <BulmaAccordionItem class>
      <h4 slot="title">The LCS</h4>
      <i slot="icon-open" class="material-icons">Click for Less</i>
      <i slot="icon-closed" class="material-icons">Click for More</i>
      <div slot="content">
        <p class="firstP">
          What the LCS is: it is an assessment of how one learns and
          communicates. It is based on the triunal brain system, meaning that
          there are three parts of the brain that control three specific
          processes. These three centers are measured by this assessment and the
          information determines a series of unique learning and communication
          sequences that cut right to the heart of the individual and how they
          are performing.
        </p>
        <br />

        <p>
          There are some very fine personality tests out there on the market
          today that give you so much information it is hard to weed through to
          the essentials of what you want to know about yourself and others. The
          LCS is different. In a few hours, you are an expert, and in those same
          few hours, you have the answers you've been seeking about yourself,
          your talents, gifts and abilities, your ability to process mental,
          emotional and physical information, how fast you are in each of these
          areas, what your inclinations are and how you will be inclined to
          behave in any given circumstance. Employers will learn that the job
          they have to offer has an LCS and a successful hire is matching the
          right candidate's LCS to the job's LCS. This assessment can also tell
          an employer who's going to be the most productive, who can handle more
          stress without falling apart, who will work well with others, keep a
          positive attitude, and what he can expect from this employee in a
          crisis. This assessment shows what the individual's weaknesses and
          strengths are and how to minimize and amplify them respectively. It
          will enhance extremely effective communication, eliminate
          misunderstandings between people, deepen teamwork remarkably, lessen
          frustration in the workplace and much more.
        </p>
        <br />
      </div>
    </BulmaAccordionItem>
    <!-- eslint-enable -->
  </BulmaAccordion>
</template>
<script>
export default {
  name: 'LCS'
}
</script>
