<template>
  <div class="logo-wrapper">
    <img src="~/assets/m-logo-circle-fill-about-png-final.png" alt spin />
    <h2 class="logoText">
      Martha Novak
    </h2>

    <!-- <img
      class="marthaTextLogo"
      src="~/static/logo-frames/MTextLogo.png"
      alt=""
    />-->
  </div>
</template>
<script>
export default {
  name: 'SiteLogo',
  data() {
    return {
      frames: 5,
      currentFrame: 1,
      blinking: true
    }
  },
  mounted() {
    setInterval(() => {
      const rand = Math.ceil(Math.random() * 10)
      this.blinking = rand % 2
    }, 1000)
  }
}
</script>
<style scoped>
.navbar-item img {
  max-height: 5.3rem;
  margin-left: 10%;
}

.logo-wrapper {
  position: absolute;
  height: 173px;
  overflow: hidden;
  width: 400px;
  top: 5%;
}

img.marthaTextLogo {
  margin-left: 61%;
}
h2.logoText {
  display: inline-block !important;
  top: 7%;
  color: #363636;
  font-size: 27px;
  font-weight: 500;
  position: absolute;
  margin-left: 6%;
}
@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  .navbar-item img {
    width: 2.5rem;
    margin-left: 2%;
    margin-top: 2%;
  }
  h2.logoText {
    font-size: 23px;
    margin-left: 2%;
  }
}
</style>
