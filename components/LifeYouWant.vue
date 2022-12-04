<template>
  <section class="section">
    <div class="teacup container">
      <h2 class="title center">
        The Life You Want
      </h2>
      <hr />
      <!-- eslint-disable -->
      <div class="columns">
        <div class="column iframe">
          <img class="teacupImg" :srcset="require('~/assets/lifeyouwant.jpg').srcSet" alt />
        </div>
        <div class="column teacupQuote">
          <p class="container-paragraphs">
            Nothing is as it seems in this world. Many of us have had
            extraordinary experiences where we've glimpsed this reality --
            mystical peeks behind the ordinary, life-threatening moments that
            alter us forever, or a moment in nature of profound communion. The
            many revelations in this book take you behind the appearance of
            things, into the workings of energy and a radical perspective on the
            way things truly are. Call it enlightenment, greater consciousness
            or living in grace, it is a potential available to all.
          </p>
          <p>
            Martha Novak’s “The Life You Want” delves into the subject of
            greater consciousness and extraordinary, untapped human potential.
            This book will dismantle your old, limited beliefs about the nature
            of who you are, the possibility of real love, and will give you
            answers from the perspective of how you use your energy to
            perpetuate the past rather than create a truly different present and
            future. It will lead you to a new understanding of deeper realities
            which can actually be seen and understood, realitieswhich are hidden
            beneath the surface of human relationships and beneath every
            person's struggle to find meaning and happiness.
          </p>
          <p>
            The author has a unique capacity for translating complex concepts,
            offering practical approaches which you can immediately incorporate.
            She takes the stories of everyday life showing us how we trap our
            energies as we hold onto the past, secured to the beliefs we
            conjured as children, remaining energetically hostage to images and
            ideas that were never even ours to begin with. Only when we bring
            our energy into the present, do we live our lives passionately,
            joyously, creatively and far more lovingly according to our true
            nature. You can purchase Martha's book now on amazon.com, kindle.com
            or at The Phoenix and Dragon Bookstore in Sandy Springs,GA.!
          </p>
        </div>
      </div>
      <ul class="teacupPurchasButtons life">
        <li class="amazonBut">
          <a
            href="https://www.amazon.com/Life-Want-Martha-Burgess-Novak/dp/1491232137/ref=sr_1_1?s=books&ie=UTF8&qid=1395173703&sr=1-1&keywords=martha+burgess+novak"
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
        <li class="amazonBut">
          <a
            href="https://www.kirkusreviews.com/book-reviews/martha-burgess-novak/the-life-you-want/"
            class="teacuplink"
            target="_blank"
          >Kirkus Review</a>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import axios from 'axios'

export default {
  name: 'LifeYouWant',
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
  margin-top: -10%;
  margin-left: 35%;
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
.teacupPurchasButtons.life {
  margin-top: -5%;
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
  .title {
    color: #363636;
    font-size: 1.5rem;
  }
}
</style>
