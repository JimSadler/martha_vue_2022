<template>
  <section class="section">
    <div class="teacup container">
      <h2 class="title center">The Teacup Prophecies</h2>
      <hr />
      <!-- eslint-disable -->
      <div class="columns">
        <div class="column iframe">
          <img class="teacupImg mobile" :srcset="require('~/assets/teacup-cover.jpg').srcSet" alt />
        </div>
      </div>

      <p class="center" style="text-align: center; margin-bottom: 3rem;" role="presentation">
        This book is filled with ascended messages to life’s most pressing
        questions. Culled from the radio shows, teachings, writings and
        philosophy of Martha Novak, spiritual teacher, author, and lecturer,
        these answers will take you to the center of who you are as your Highest
        Self and, from an egoic perspective, they will challenge you to be more.
        Each message is teacup size, sometimes esoteric and sometimes triggering
        more than a little thought. Don’t be deceived by their size, these
        little tidbits, they pack a punch. Rest assured, it will be your
        message, just for you, made possible and brought to you by… you.
      </p>

      <div class="columns">
        <div class="column iframe">
          <img class="teacupImg desktop" :srcset="require('~/assets/teacup-cover.jpg').srcSet" alt />
        </div>
        <div class="column teacupQuote">
          <div class="column">
            <ul class="teacupButtons">
              <li>
                <div class="teacupButton">
                  <button @click="getTeacupData">
                    <div class="teacupImage">
                      <img
                        class="teacupButtImg"
                        :srcset="
                          require('~/assets/coffee-icon-png-5.png').srcSet
                        "
                        alt
                      />
                    </div>
                    <span class="teacupButText">Get Quote</span>
                  </button>
                </div>
              </li>
            </ul>
          </div>
          <div class="column">
            <div class="teacup-data">
              <blockquote class="quote" cite="Martha Novak">{{ randomQuote }}</blockquote>
              <span cite="Martha Novak"></span>
            </div>
          </div>
        </div>
      </div>

      <ul class="teacupPurchasButtons">
        <hr />
        <li class="amazonBut">
          <a
            href="https://www.amazon.com/dp/B01N7H96KP/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1"
            class="teacuplink"
            target="_blank"
          >Buy on Amazon</a>
        </li>
        <li class="amazonBut e-book">
          <a
            href="https://www.amazon.com/dp/B00J6F46UU"
            class="teacuplink"
            target="_blank"
          >Buy E-book</a>
        </li>
        <!-- <li class="appstore">
          <a
            href="https://itunes.apple.com/us/app/the-teacup-prophecies/id1332467134?ls=1&mt=8"
          >
            <img
              class="appstorebutt"
              :srcset="require('~/static/button-appstore.png').srcSet"
              alt=""
            />
          </a>
        </li>-->
        <a href="https://itunes.apple.com/us/app/the-teacup-prophecies/id1332467134?ls=1&mt=8">
          <img class="appstorebutt" :srcset="require('~/static/button-appstore.png').srcSet" alt />
        </a>
      </ul>
    </div>
  </section>
</template>

<script>
import axios from 'axios'

export default {
  name: 'Teacup',
  data() {
    return {
      teacupDataList: []
    }
  },
  computed: {
    randomQuote() {
      const rand = Math.floor(Math.random() * this.teacupDataList.length)
      return this.teacupDataList[rand] ? this.teacupDataList[rand].quote : ''
    }
  },

  methods: {
    getTeacupData() {
      axios.get('/teacupProph.json').then((response) => {
        this.teacupDataList = response.data
      })
    }
  }
}
</script>
<style scoped>
.quote {
  margin: 5%;
}
li.amazonBut.e-book {
  padding-right: 3%;
  padding-left: 3%;
}
blockquote {
  display: block;
  border-width: 2px 0;
  border-style: solid;
  border-color: #eee;
  padding: 1.5em 0 0.5em;
  margin: 1.5em 0;
  position: relative;
}
blockquote:before {
  content: '\201C';
  position: absolute;
  top: 0em;
  left: 50%;
  transform: translate(-50%, -50%);
  background: #fff;
  width: 3rem;
  height: 2rem;
  font: 6em/1.08em 'PT Sans', sans-serif;
  color: #666;
  text-align: center;
}
blockquote + span:after {
  content: '\2013 \2003'attr(cite);
  display: block;
  text-align: right;
  font-size: 1em;
  color: #363636;
}
.componet_sub {
  margin-top: 3% !important;
}
.teacup-data {
  padding: 2%;
  /* border: solid #363636 1px; */
}
.teacupButton {
  margin-top: -20%;
  text-align: center;
}
.teacupButton a {
  padding-left: 5%;
}
/* img.teacupImg {
  height: auto;
  max-width: 32%;
} */
.subtitle {
  font-size: 1rem;
  text-align: center;
}
.teacup.container h2,
.teacup.container h3 {
  text-align: center;
}
.teacup.container h3 {
  margin-bottom: 5%;
}
.teacup.container {
  margin-bottom: 0%;
}
.teacupButton button {
  -webkit-transition: 0.6s;
  transition: 0.6s;
  background-color: #8db0b3;
  color: white;
  border: 1px solid #ccc;
  border-radius: 5px;
  /* display: inline-block; */
  text-decoration: none;
  color: rgba(152, 152, 152, 0.43);
  width: 160px;
  height: auto;
  /* line-height: 80px; */
  text-align: center;
  vertical-align: middle;
  overflow: hidden;
  font-weight: bold;
  /* text-shadow: 1px 1px 1px rgba(255, 255, 255, 0.66); */
  /* box-shadow: inset 0 2px 0 rgba(255, 255, 255, 0.5), 0 2px 2px rgba(0, 0, 0, 0.19); */
  /* border-bottom: solid 2px #b5b5b5; */
}
.teacupButt2 {
  background-color: #8db0b3;
  color: white;
  border: 1px solid #ccc;
  border-radius: 5px;
}
[data-icon='mug-hot'] {
  font-size: 28px;
  color: #363636;
  transition: 0.6s;
}
img.teacupButtImg {
  width: 27%;
}
.column.teacupQuote {
  margin-left: -29%;
}
.teacupQuote .columns.CTAButtons {
  margin-top: 0%;
}
.teacupButtons {
  text-align: center;
  margin-top: 6%;
  margin-left: 0%;
}
ul.teacupPurchasButtons {
  text-align: center;
  margin-left: 35%;
  margin-top: 2%;
}
.teacupButtons li,
.teacupPurchasButtons li {
  text-align: center;
  display: inline-block;
  padding: 13px;
}
.teacupPurchasButtons li {
  margin-right: 1%;
  margin-left: 1%;
}
.teacupButText {
  display: inline-block;
  font-size: 13px;
  color: #363636;
  transition: 0.6s;
}
li.appstore {
  width: 150px;
}
.amazonBut {
  position: relative;
  display: inline-block;
  font-weight: bold;
  text-decoration: none;
  color: #fff;
  text-shadow: 0 0 5px rgba(255, 255, 255, 0.73);
  border-radius: 5px;
  border: 1px solid #363636;
  /* background: #8db0b2; */
  font-size: 13px;
  transition: 0.6s;
}
.teacupButton button:hover {
  background-color: #363636;
  color: whitesmoke;
}
.teacupButton:hover .teacupButText {
  color: whitesmoke;
  text-shadow: -6px 0px 15px rgba(255, 255, 240, 0.83),
    6px 0px 15px rgba(255, 255, 240, 0.83);
}
.teacupButton:hover [data-icon='mug-hot'] {
  font-size: 28px;
  color: whitesmoke;
}
img.teacupButtImg {
  transition: 0.6s;
}
.teacupButton:hover img.teacupButtImg {
  filter: invert(1);
  transition: 0.8s;
}
.appstorebutt {
  filter: invert(1);
}
.appstorebutt:hover {
  filter: invert(0);
  transition: 0.8s;
}
a.teacuplink {
  color: #363636;
  cursor: pointer;
  text-decoration: none;
  transition: 0.6s;
}
.amazonBut:hover {
  text-shadow: -6px 0px 15px rgba(255, 255, 240, 0.83),
    6px 0px 15px rgba(255, 255, 240, 0.83);
  background-color: #363636;
  color: whitesmoke !important;
}
.amazonBut:hover a.teacuplink {
  color: whitesmoke !important;
}
.teacupImg {
  width: 41%;
}
/* img.appstorebutt {
  width: 29%;
} */
img.appstorebutt {
  width: 12%;
  margin-left: 1%;
  position: absolute;
  transition: 0.8s;
}
.teacupImg.mobile {
  display: none;
}
.teacupImg.desktop {
  display: block;
}
@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  .column.teacupQuote {
    margin-left: 0%;
  }
  .column.iframe {
    text-align: center;
  }
  .teacupImg {
    width: 100%;
  }
  .teacupImg.mobile {
    display: block;
  }
  .teacupImg.desktop {
    display: none;
  }
  .title {
    color: #363636;
    font-size: 1.5rem;
  }
  .teacupPurchasButtons li[data-v-74581e49] {
    margin-right: 0%;
    margin-left: 0%;
    width: 100%;
  }
  ul.teacupPurchasButtons {
    margin-left: 0%;
  }
  .appstorebutt {
    max-width: 60%;
  }
}
</style>
