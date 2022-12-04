<template>
  <div id="workshop-page">
    <site-hero title="Classes" image="/uploads/hawaii-4923130_1920.jpg">
    </site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="columns">
          <div class="column is-full">
            <h3>2019 Class Information</h3>
            <hr />
          </div>
        </div>
        <div class="card">
          <div class="card-content">
            <div class="media">
              <div class="media-left">
                <font-awesome-icon
                  icon="calendar-alt"
                  style="margin-right: 10px;"
                  size="2x"
                />
              </div>
              <div class="media-content">
                <p class="title is-4">
                  Basic Format Class
                </p>
                <p class="subtitle is-6">
                  Watch for announcements soon about upcoming dates and times!
                </p>
                <p>Cost: $695</p>
              </div>
              <!-- <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time> -->
            </div>

            <div class="content">
              <p>
                This is a broadcast class. You may take it online or in person.
              </p>
              <p>
                This class will introduce you to how energetic healings take
                place in this method. You will be emailed a basic format sheet
                that you will be used in many other classes should you decide to
                study further with Martha.
              </p>
              <p>
                In all honesty, this is a hard class. You will be stretched in
                this class and, make no mistake about it, you will not be an
                adept at format when you finish. This is just as it should be as
                this class is an introduction to your gifts and how to apply
                them in a very specific way. Through the years, students of ours
                have struggled with this class and mastered it in a few months,
                but it does take those few months of commitment and practice.
              </p>

              <p>
                There will be support classes to follow if this is the course of
                study you choose, all taught by Martha. She likes to know her
                students and watch their progress as the facilitator/healers in
                her organization come out of these classes.
              </p>
              <p>
                There is one prerequisite for these classes. You must be willing
                to work with one of Martha's facilitator/healers starting two
                weeks before the class begins and for the duration of the class.
                Of course, we hope you'll go on with your facilitator/healer
                after the class is over but this will be your choice. Count, in
                addition to the $695 cost of the class, another $150 a week for
                a full two hour session with one of the accredited
                facilitators/healers.
              </p>
              <br />
            </div>
            <form
              action="https://www.paypal.com/cgi-bin/webscr"
              method="post"
              target="_top"
            >
              <input type="hidden" name="cmd" value="_s-xclick" />
              <input
                type="hidden"
                name="hosted_button_id"
                value="HYHD6RJN4JZH6"
              />
              <input
                class="buyNowButton"
                type="image"
                src="https://dabuttonfactory.com/button.png?t=Buy+Now&f=Droid+Serif-Bold&ts=15&tc=fff&tshs=1&tshc=000&hp=20&vp=8&c=5&bgt=gradient&bgc=073763&ebgc=0f7283"
                border="0"
                name="submit"
                alt="PayPal - The safer, easier way to pay online!"
              />
              <img
                alt
                border="0"
                src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif"
                width="1"
                height="1"
              />
            </form>
          </div>
        </div>
        <div class="card">
          <div class="card-content">
            <div class="media">
              <div class="media-left">
                <font-awesome-icon
                  icon="calendar-alt"
                  style="margin-right: 10px;"
                  size="2x"
                />
              </div>
              <div class="media-content">
                <p class="title is-4">
                  Basic Format Class
                </p>
                <p class="subtitle is-6">
                  Watch for announcements soon about upcoming dates and times!
                </p>
                <p>Cost: $795 ( cost of auditing this class is $625)</p>
              </div>
              <!-- <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time> -->
            </div>

            <div class="content">
              <p class="editable">
                This is a broadcast class. You may take it online or in person.
              </p>
              <p class="editable">
                The emphasis of this class is on the deeply psychological wiring
                of the ego and the egoic child's mind. We analyze, facilitate
                healing, uncover deeply buried, convoluted beliefs that limit us
                and help each other grow, change and become authentic as the
                spiritual beings in physical form we are. This class teaches and
                inspires and the vastness of The Burgess Process and the varied
                techniques and powerful processes are revealed in this class. We
                say "over time" because we have a mass of material to cover,
                there's no way it can begin to be covered in one class, and this
                is why this is an on-going class for the serious student of
                consciousness. Each quarter we pick up where we left off and
                each quarter we go deeper into more esoteric, applicable study.
              </p>
              <p class="editable">
                It is possible for eager format students to audit this class. Be
                advised, however, this is a class we recommend you work up to
                through the other class offerings and your private sessions.
              </p>
              <br />
              <form
                action="https://www.paypal.com/cgi-bin/webscr"
                method="post"
                target="_top"
              >
                <input type="hidden" name="cmd" value="_s-xclick" />
                <input
                  type="hidden"
                  name="hosted_button_id"
                  value="3EKLKZ48XQ6JY"
                />
                <input
                  class="buyNowButton"
                  type="image"
                  src="https://dabuttonfactory.com/button.png?t=Buy+Now&f=Droid+Serif-Bold&ts=15&tc=fff&tshs=1&tshc=000&hp=20&vp=8&c=5&bgt=gradient&bgc=073763&ebgc=0f7283"
                  border="0"
                  name="submit"
                  alt="PayPal - The safer, easier way to pay online!"
                />
                <img
                  alt
                  border="0"
                  src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif"
                  width="1"
                  height="1"
                />
              </form>
            </div>
          </div>
        </div>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <!-- Latest Posts -->
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
// import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `Classes | ${this.$siteConfig.siteName}`
    }
  }
  // components: { QuoteCard }
}
</script>
<style scoped>
.testimonials {
  font-weight: 500;
  font-size: 18px;
}
input.buyNowButton,
a button.buyNow {
  -webkit-filter: grayscale(1);
  transition: 0.8s;
}
input.buyNowButton:hover,
a button.buyNow:hover {
  -webkit-filter: grayscale(0);
}
.panel-body form {
  text-align: center;
}
.card {
  margin-top: 3%;
  margin-bottom: 3%;
}
</style>
