<template>
  <section class="section youtube">
    <div class="container">
      <h2 class="title youtubeHeader">Radio Show</h2>
      <div class="columns fadeInUp animated">
        <div class="column iframe">
          <iframe
            width="640"
            height="480"
            src="https://www.youtube.com/embed/AMFgcQ1v1w0?start=658&amp;end=699"
            frameborder="0"
            allow="autoplay; encrypted-media"
            allowfullscreen
          ></iframe>
        </div>
        <div class="column ctabox">
          <h2 class="title center">What Is Consciousness?</h2>
          <h3 class="subtitle center">Real Talk Sundays at 10AM ET</h3>
          <div class="columns CTAButtons">
            <div class="column">
              <button
                role="link"
                onclick="window.open('https://www.blogtalkradio.com/marthanovak/','_blank');"
                class="btn btn-sm animated-button victoria-three animated flipInX"
              >Listen to the Show</button>
            </div>
            <div class="column faceLiveButton">
              <button
                role="link"
                onclick="window.open('https://www.facebook.com/RealTalkwithMartha/','_blank');"
                class="btn btn-sm animated-button victoria-three animated flipInX"
              >Facebook Live</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'YouTubeCTA2'
}
</script>

<style scoped>
.youtubeHeader {
  text-align: center;
  margin-bottom: 5%;
}
.ctabox {
  border: solid 1px #363636;
  border-radius: 5px;
}
.columns.CTAButtons {
  padding-top: 10%;
}
.button2 {
  float: left;
}
.button1 {
  float: right;
}
.column.iframe {
  padding: 0px;
}
img,
embed,
iframe,
object,
video {
  height: 100%;
  max-width: 100%;
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
  /* border: 2px solid #0e7283; */
  width: 12.5em;
  background-color: whitesmoke;
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
.center {
  text-align: center;
  margin-top: 15%;
}
section.youtube {
  margin-top: 2%;
  margin-bottom: 2%;
  /* background-color: #eeeeee; */
  /* background-size: cover; */
}
</style>
