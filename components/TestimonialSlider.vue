<template>
  <div>
    <section class="testSlider">
      <h2>Testimonials</h2>
      <client-only>
        <flickity
          id="testSlide"
          ref="flickity"
          class="flickity"
          :options="flickityOptions"
        >
          <div class="carousel-cell background-slide1">
            <div class="transbox">
              <h2 class="testimonials">
                Randall P. Martin, Investment Adviser, Atlanta, Ga.
              </h2>
              <p class="container-paragraphs">
                Martha has transformed my life with her powerful energy work.
                She is love personified, radiant from the heart, wise, kind,
                intellectually brilliant and psychically gifted. I recommend her
                unequivocably.
              </p>
              <div class="transboxButton"></div>
            </div>
            <!-- <div class="bg-img"></div> -->
            <img class="carouselImg" alt="" />
          </div>
          <div class="carousel-cell background-slide2">
            <div class="transbox">
              <h2 class="testimonials">
                Hope Merrill, Owner and Founder of The Conscious Life Journal.
              </h2>
              <p class="container-paragraphs">
                "A mutual friend said to me with admiration, “Martha Novak is a
                force of nature!” I smiled with recognition of a fellow Martha
                fan and quickly agreed wholeheartedly. Martha is indeed a
                treasure who manages to exemplify the delicate balance of living
                life as a conscious human. She is sharp, and bright, and
                articulate while being simultaneously warm, compassionate and
                unbelievably charming. She challenges you, guides you, educates
                you and applauds your inevitable transformation under her care.
                When you are ready, when it is time for you to live the life you
                really want to live, then you will find her, or one of her many
                master graduate students, and your life will simply never be the
                same. Her Infinite Insight is complete, brilliant, and unique.
                And the results, well, for me they were nothing short of
                miraculous. My undying gratitude to, and for, this beautiful,
                authentic woman!"
              </p>
            </div>

            <img class="carouselImg" />
          </div>
          <div class="carousel-cell background-slide3">
            <div class="transbox">
              <h2 class="testimonials">
                Hugh Switzer, Retired Executive, The Coca Cola Company
              </h2>
              <p class="container-paragraphs">
                My wife has been into consciousness raising for years. I've
                accompanied her to this and that, and so I thought I was going
                along for another nice ride when she found Martha Burgess Novak
                and The Burgess Process. Right away, Martha and her work spoke
                to me as a man, as a husband, and as a father. I was truly blown
                away. Since that time, I have joined Martha in her classes, in
                her lectures, and in her private sessions. Her insight is
                amazing and she really does teach you how to live in joy, love,
                peace and harmony with ourselves, other people and our God.
                Martha doesn't just tell you "it's out there" for you. She gives
                you the practical, step by step approaches to get there,
                encouraging you fully along the way. I'd recommend her and this
                work to every man out there. Instead of waiting for your wives
                to initiate... this time, take your wives!
              </p>
            </div>

            <img class="carouselImg" alt="" />
          </div>
        </flickity>
      </client-only>
    </section>
  </div>
</template>

<script>
export default {
  name: 'TesimonialSlider',
  data() {
    return {
      flickityOptions: {
        initialIndex: 3,
        prevNextButtons: true,
        pageDots: true,
        autoPlay: 30000,
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

<style lang="scss" scoped>
.testSlider h2 {
  text-align: center;
  font-size: 26px;
  font-weight: 600;

  padding-top: 2%;
}
#testSlide h2.testimonials {
  font-size: 18px;
  font-weight: 500;
}
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

.testSlider #testSlide .flickity-viewport {
  min-height: 500px !important;
}
#testSlide .carousel-cell {
  width: 100%; /* full width */
  margin-right: 10px;
  min-height: 50%;
  margin-top: 4%;
  border: none;
}
.testSlider {
  background-color: lightgray;
  height: 531px;
  margin-bottom: 0%;
}
#testSlide div.transbox {
  margin: 2% 10%;
  border: none;

  /* background-color: #ffffff; */
  /* border: 1px solid black; */
  /* opacity: 0.7;
  filter: alpha(opacity=60); */
  text-align: center;
}

#testSlide div.transbox p {
  // margin: 15%;
  // font-weight: bold;
  color: #363636;
}
// div.transbox h2 {
//   margin: 22% 14% 2% 14%;
//   font-size: 45px;
//   font-weight: bold;
//   color: whitesmoke;
// }
.bg-img {
  width: 100%;
  height: 100%;
  // background-image: linear-gradient(to bottom right, #002f4b, #131212);
  opacity: 0.6;
  background-size: cover;
  background-color: transparent;
  // filter: grayscale(1);
  // &:before {
  //   content: '';
  //   position: absolute;
  //   top: 0;
  //   right: 0;
  //   bottom: 0;
  //   left: 0;
  //   background-image: linear-gradient(to bottom right, #002f4b, #131212);
  //   opacity: 0.6;
  // }
}
button.button {
  margin-left: 75%;
}
flickity {
  display: block;
}
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
  left: 10px;
}
.flickity-prev-next-button.next {
  right: 10px;
}
.flickity-prev-next-button {
  top: 50%;
  width: 44px;
  height: 44px;
  border-radius: 50%;
  transform: translateY(-50%);
  webkit-transform: translateY(-50%);
}
.flickity-button {
  position: absolute;
  background: hsla(0, 0%, 100%, 0.75);
  border: none;
  color: #333;
}
.flickity-prev-next-button .flickity-button-icon {
  position: absolute;
  left: 20%;
  top: 20%;
  width: 60%;
  height: 60%;
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
</style>
