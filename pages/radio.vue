<template>
  <div id="#radio-page">
    <site-hero-large
      title="Radio Show"
      subtitle="Blog Talk Radio and Facebook Live Weekly Show "
      image="/uploads/Radio Show/eurasian-wigeon-4914971_1920.png"
    >
      <h3 class="sub-page-header" role="presentation">
        Sundays at 10AM ET
      </h3>
    </site-hero-large>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <section class="is-large">
          <div class="container radioShow">
            <div class="column is-full">
              <h2 class="page-header">
                Show Dates
              </h2>
              <hr />
            </div>
            <div>
              <p>
                Martha's broadcasts are on Blog Talk Radio and Facebook Live and
                her shows , on a variety of subjects, are archived on these
                channels and on YouTube. All broadcasts are free. Thank you for
                telling others about Martha and these great shows. We appreciate
                it!
              </p>
            </div>
            <!-- eslint-disable -->
            <ul class="showList">

              <li v-for="item in radio_descriptions" :key="item">
                <h3 role="presentation">{{ item.date }}</h3>
                <p>
                  {{item.description}}
                </p>
              </li>


              <!-- <li>
                <h3 role="presentation">07/10/22</h3>
                <p>
                  Martha is taking this week off, July 10th. Please visit her
                  archived shows! She'll be back with a live show on Blog Talk
                  Radio and Facebook Live on Sunday, June 26th
                </p>
              </li> -->

            </ul>

            <div class="columns">
              <!-- eslint-disable -->
              <div class="column radShowButton">
                <button
                  role="link"
                  onclick="window.open('https://www.blogtalkradio.com/marthanovak/2023/03/05/real-talk-with-martha-novak','_blank');"
                  class="btn btn-sm animated-button victoria-three animated flipInX"
                >
                  Listen to the Show
                </button>
              </div>
              <div class="column faceLiveButton">
                <button
                  role="link"
                  onclick="window.open('https://www.facebook.com/RealTalkwithMartha/','_blank');"
                  class="btn btn-sm animated-button victoria-three animated flipInX"
                >
                  Facebook Live
                </button>
              </div>
            </div>
            <hr />
            <p>
              All Martha's shows are archived on Blog Talk Radio, Facebook Live
              and YouTube so do please check out past shows. We also encourage
              you to form study groups around these shows to support your
              journey. Thank you so much for following Martha, befriending her
              (Martha Novak on FB), sharing these shows, and liking them. Your
              kindness in taking time to do these things increases our number of
              listeners and helps get the word around. We appreciate it! There
              are all sorts of information and consciousness tools on this site
              (CDs, DVDs, books, and a fabulous app for iPhones that is only .99
              and extremely fun to use).
            </p>
          </div>
        </section>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">Latest Posts</h3>
        <!-- Latest Posts -->
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import SiteHeroLarge from '~/components/SiteHeroLg'
export default {
  components: {
    SiteHeroLarge
  },
  data() {
    return {
      radio_descriptions: [
        {
          date: '03/05/23',
          description:
            "Dears, This is Martha and I do want to report what's going on right now. The flu I thought I had got much worse. I ended up in the hospital for 3 days with pneumonia. I came home Thursday, but am still very, very weak and sick. I'm going to take a month off from REAL TALK with Martha Novak to get over this. Please look for a new notice for the week of March 27th about a possible April 2nd show. I'll miss you this month and wish you all great health and happiness.Love, Martha Novak "
        },
        {
          date: '04/02/23',
          description: 'Coming Soon'
        }
      ]
    }
  },
  head() {
    return {
      title: `Radio Show | ${this.$siteConfig.siteName}`
    }
  }
}
</script>

<style scoped>
.radioShow {
  padding-top: 3%;
  padding-bottom: 5%;
}
.column.radShowButton button {
  float: right;
}
h2.page-header {
  font-size: 26px;
  text-align: center;
}
h3.sub-page-header {
  font-size: 18px;
  text-align: left;
}
.showList li {
  padding: 2% 5%;
}
.showList h3 {
  font-size: 18px;
  font-weight: 500;
}
/* Animated Buttons */
#radio-page a.animated-button,
#radio-page a.animated-button:visited,
#radio-pagebutton.animated-button,
#radio-page button.animated-button:visited {
  position: relative;
  /*display: block;*/
  margin: 20px auto 0;
  padding: 14px 15px !important;
  color: black;
  font-size: 14px;
  /*font-weight: bold;*/
  text-align: center;
  text-decoration: none;
  overflow: hidden;
  letter-spacing: 0.08em;
  border-radius: 7px;
  text-shadow: 0 0 1px rgba(0, 0, 0, 0.2), 0 1px 0 rgba(0, 0, 0, 0.2);
  -webkit-transition: all 1s ease;
  -moz-transition: all 1s ease;
  -o-transition: all 1s ease;
  transition: all 1s ease;
}
a.animated-button:after,
a.animated-button:visited:after,
button.animated-button:after,
button.animated-button:visited:after {
  content: '';
  position: absolute;
  height: 0%;
  left: 50%;
  top: 50%;
  width: 150%;
  z-index: -1;
  -webkit-transition: all 0.75s ease 0s;
  -moz-transition: all 0.75s ease 0s;
  -o-transition: all 0.75s ease 0s;
  transition: all 0.75s ease 0s;
}
a.animated-button:hover,
a.animated-button:visited:hover,
button.animated-button:visited:hover,
button.animated-button:hover {
  color: #fff;
  text-shadow: none;
  background-color: #0e7283;
}
a.animated-button:hover:after,
a.animated-button:visited:hover:after,
button.animated-button:hover:after,
button.animated-button:visited:hover:after {
  height: 450%;
}

/* Sandy Buttons */
a.animated-button.victoria-three,
button.animated-button.victoria-three {
  border: 2px solid #0e7283;
  width: 12.5em;
}
a.animated-button.victoria-three:after,
button.animated-button.victoria-three:after {
  background: #0e7283;
  opacity: 0.5;
  -moz-transform: translateX(-50%) translateY(-50%);
  -ms-transform: translateX(-50%) translateY(-50%);
  -webkit-transform: translateX(-50%) translateY(-50%);
  transform: translateX(-50%) translateY(-50%);
}
a.animated-button.victoria-three:hover:after,
button.animated-button.victoria-three:hover:after {
  height: 140%;
  opacity: 1;
}
@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  a.animated-button.victoria-three,
  button.animated-button.victoria-three {
    border: 2px solid #0e7283;
    background: #0e7283;
    width: 23.5em;
    color: #333;
  }
}
</style>
