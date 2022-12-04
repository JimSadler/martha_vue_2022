<template>
  <!-- eslint-disable -->
  <div>
    <client-only>
      <flickity
        id="homeSlider"
        ref="flickity"
        class="flickity"
        :options="flickityOptions"
      >
        <div class="carousel-cell background-slide1">
          <div class="transbox" style="text-align: center;">
            <h2>
              Listen to Martha’s Radio Show for powerful information and
              uplifting insights.
              <br />Open your awareness.
              <!-- <button class="button">Learn More</button> -->
              <br />

              <nuxt-link
                class="button btn is-medium animated-button victoria-three animated flipInX"
                to="/radio"
                >Explore Here</nuxt-link
              >
            </h2>
          </div>
          <!-- <div class="bg-img"></div> -->
          <img
            class="carouselImg"
            :srcset="require('~/static/homepage/tulip-2189317_1920.jpg').srcSet"
            alt
          />
        </div>
        <div class="carousel-cell background-slide2">
          <div class="transbox" style="text-align: center;">
            <h2>
              Wherever you are on your spiritual journey
              <br />private sessions are available.
              <br />
              <span class="slidersubHead">Discover yourself.</span>
              <!-- <button class="button">Learn More</button> -->
              <br />
              <nuxt-link
                class="button btn is-medium animated-button victoria-three animated flipInX"
                to="/about"
                >Connect Here</nuxt-link
              >
            </h2>
          </div>

          <img
            class="carouselImg"
            :srcset="
              require('~/static/homepage/hummingbird-2139279_1920.jpg').srcSet
            "
            alt
          />
        </div>
        <div class="carousel-cell background-slide3">
          <div class="transbox" style="text-align: center;">
            <h2>
              Unlock your potential
              <br />through personal growth and change. <br />Courses and media
              downloads available.
              <!-- <button class="button">Learn More</button> -->
              <br />
              <nuxt-link
                class="button btn is-medium animated-button victoria-three animated flipInX"
                to="/classes"
                >Learn More</nuxt-link
              >
            </h2>
            <div class="transboxButton"></div>
          </div>
          <img
            class="carouselImg"
            :srcset="
              require('~/static/homepage/milky-way-916523_1920.jpg').srcSet
            "
            alt
          />
        </div>
      </flickity>
    </client-only>
  </div>
</template>

<script>
export default {
  data() {
    return {
      flickityOptions: {
        initialIndex: 3,
        prevNextButtons: true,
        pageDots: false,
        autoPlay: 8000,
        freeScroll: true,
        selectedAttraction: 0.01,
        friction: 0.15,
        wrapAround: true
        // any options from Flickity can be used
      }
    }
  }
}
</script>

<style lang="scss">
.carouselImg {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  object-fit: cover;
  width: 100%;
  height: 100%;
  z-index: -1;
}
// .flickity {
//   // margin-top: 2%;
//   // min-height: 100vh;
// }
#homeSlider .flickity-viewport {
  min-height: 100vh;
}
#homeSlider .carousel-cell {
  width: 100%; /* full width */
  margin-right: 10px;
  min-height: 100vh;
}

#homeSlider div.transbox {
  margin-left: 35%;
  margin-top: 30%;
  // background-color: #ffffff;
  // border: 1px solid black;
  // opacity: 0.7;
  // filter: alpha(opacity=60);
  text-align: right;
}

#homeSlider div.transbox p {
  margin: 15%;
  font-weight: bold;
  color: whitesmoke;
}
#homeSlider div.transbox h2 {
  margin: 22% 10% 2% 30%;
  font-size: 35px;
  font-weight: 200;
  color: whitesmoke;
}
#homeSlider .transbox .button {
  font-weight: 500;
}
.bg-img {
  width: 100%;
  height: 100%;
  background-image: linear-gradient(to bottom right, #002f4b, #131212);
  opacity: 0.6;
  background-size: cover;
}
button.button {
  margin-left: 75%;
}
// flickity {
//   display: block;
// }
.flickity-page-dots .dot {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 0 8px;
  background: #333;
  border-radius: 50%;
  opacity: 0.25;
  cursor: pointer;
}
.flickity-page-dots .dot.is-selected {
  opacity: 1;
}
.flickity-page-dots {
  position: absolute;
  width: 100%;
  bottom: -25px;
  padding: 0;
  margin: 0;
  list-style: none;
  text-align: center;
  line-height: 1;
}
.flickity-prev-next-button.previous {
  left: 2rem;
}
.flickity-prev-next-button.next {
  right: 2rem;
}

.flickity-prev-next-button {
  top: 50%;
  width: 55px;
  height: 55px;
  border-radius: 50%;
  transform: translateY(-50%);
}
.flickity-button {
  position: absolute;
  background: transparent !important;
  border: none;
  color: #333;
}
.flickity-button:hover {
  background: transparent !important;
  cursor: pointer;
}
.flickity-prev-next-button .flickity-button-icon {
  position: absolute;
  left: 20%;
  top: 20%;
  width: 80%;
  height: 80%;
  color: whitesmoke;
  transition: 0.7s;
}
.flickity-prev-next-button:hover .flickity-button-icon {
  color: #737373;
}
.flickity-button-icon {
  fill: currentColor;
}
.flickity-enabled {
  position: relative;
}
.flickity-enabled.is-draggable {
  -webkit-tap-highlight-color: transparent;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.flickity-enabled.is-draggable .flickity-viewport {
  cursor: move;
  cursor: -webkit-grab;
  cursor: grab;
}
.flickity-slider {
  position: absolute;
  width: 100%;
  height: 100%;
}
.transbox a.button {
  margin-top: 2%;
}
/* Animated Buttons */
a.animated-button,
a.animated-button:visited,
button.animated-button,
button.animated-button:visited {
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
  border: 1px solid;
  border-color: #fff !important;
}
a.animated-button:hover:after,
a.animated-button:visited:hover:after,
button.animated-button:hover:after,
button.animated-button:visited:hover:after {
  height: 450%;
}

/* Sandy Buttons */
#homeSlider a.animated-button.victoria-three,
#homeSlider button.animated-button.victoria-three {
  border: 2px solid whitesmoke;
  width: 12.5em;
  background-color: transparent;
  color: whitesmoke;
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
</style>
