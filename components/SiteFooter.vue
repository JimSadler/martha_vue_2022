<template>
  <div id="footer">
    <section class="prefooter" is-large>
      <div class="columns">
        <div class="column is-two-thirds is-full-mobile">
          <img src="~/assets/m-logo-circle-fill-about-png-final.png" alt />
          <h2 class="title">
            Martha Novak
          </h2>
        </div>
        <div class="column is-full-mobile">
          <!-- eslint-disable -->
          <ul class="social-media">
            <li>
              <a
                href="https://www.facebook.com/RealTalkwithMartha/"
                target="_blank"
                class="btn btn-facebook"
              >
                <font-awesome-icon
                  :icon="{ prefix: 'fab', iconName: 'facebook-f' }"
                />
              </a>
            </li>
            <li>
              <a
                href="https://twitter.com/MarthaBurgess"
                target="_blank"
                class="btn btn-twitter"
              >
                <font-awesome-icon
                  :icon="{ prefix: 'fab', iconName: 'twitter' }"
                />
              </a>
            </li>
            <li>
              <a
                href="https://www.linkedin.com/in/marthaburgess"
                target="_blank"
                class="btn btn-dribble"
              >
                <font-awesome-icon
                  :icon="{ prefix: 'fab', iconName: 'linkedin' }"
                />
              </a>
            </li>
            <li>
              <a
                href="https://www.youtube.com/channel/UCuNL9cW2ASL1a_slcgUKrQw"
                target="_blank"
                class="btn btn-youtube"
              >
                <font-awesome-icon
                  :icon="{ prefix: 'fab', iconName: 'youtube' }"
                />
              </a>
            </li>
            <li>
              <a
                href="https://www.meetup.com/Thursday-Night-Enlightenment/"
                target="_blank"
                class="btn btn-meetup"
              >
                <font-awesome-icon
                  :icon="{ prefix: 'fab', iconName: 'meetup' }"
                />
              </a>
            </li>
            <li>
              <a
                href="https://www.instagram.com/marthabnovak/"
                target="_blank"
                class="btn btn-insta"
              >
                <font-awesome-icon
                  :icon="{ prefix: 'fab', iconName: 'instagram' }"
                />
              </a>
            </li>
          </ul>
        </div>
      </div>
      <ul class="footerNav">
        <!-- <li class="footlink">
          <nuxt-link to="/workshops">Workshops</nuxt-link>
        </li>-->
        <!-- <li class="footlink">
          <nuxt-link to="/store">Store</nuxt-link>
        </li>-->
        <li class="footlink">
          <nuxt-link to="/contact">Contact</nuxt-link>
        </li>
        <li class="footlink">
          <nuxt-link to="/testimonial">Testimonials</nuxt-link>
        </li>
      </ul>
    </section>
    <footer class="site-footer">
      <span>
        {{ $siteConfig.siteName }} &copy; {{ new Date().getFullYear() }} - All
        Rights Reserved
      </span>
      <span>
        <br />
        <font-awesome-icon icon="cog" spin></font-awesome-icon>website developed
        by
        <div class="jsLink">
          <a target="_blank" class="animated" href="https://jsdevelopment.tech">
            <img
              id="heart"
              class="jsDevLogo animate__pulse"
              src="~/assets/uploads/jsDevLogo.png"
              alt
            />
            J.S. Development
          </a>
        </div>
      </span>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'SiteFooter'
}
</script>

<style scoped>
footer {
  /* background: #eee; */
  padding: 20px 10px;
  text-align: center;
  transition: 0.5s ease all;
}
footer a {
  text-align: center;
  color: ghostwhite;
  font-weight: 600;
  transition: 0.6s ease all;
  text-decoration: underline;
}
footer a:hover,
footer a:focus {
  color: #f9b54a;
  text-decoration: underline;
}
footer [data-icon='cog'] {
  margin-right: 0.3rem;
}
.prefooter img {
  width: 4%;
  padding-top: 1rem;
}
.prefooter h2 {
  display: inline-block;
  padding-left: 10px;
}
section.prefooter {
  padding: 20px 70px 0px;
  /* background-color: #eeeeee; */
  border-bottom: #fff 1px solid;
}
#footer {
  /* background-image: url('../static/color gradients/blue gradient 2.jpg'); */
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  background-color: #0e7283;
}
section.prefooter a {
  color: ghostwhite;
  transition: 0.5s ease all;
  font-weight: 600;
}
li.footlink {
  display: inline-block;
  padding: 10px;
}
ul.footerNav {
  /* border-bottom: 1px solid black; */
  padding: 1rem 0 2rem;
}
li.footlink a:hover,
li.footlink a:focus {
  color: #f9b54a;
  text-decoration: underline;
}
.social-media li {
  display: inline-block;
  padding: 15px;
}
ul.social-media {
  padding-top: 2rem;
}
.btn-envelope:focus,
.btn-envelope:hover {
  outline: 0;
  color: #f4f5f7;
  background-color: #41b783;
  border: solid #fff 1px;
}
.btn-facebook:focus,
.btn-facebook:hover {
  outline: 0;
  color: #f4f5f7;
  background-color: #3b5998 !important;
  border: solid #fff 1px;
}
.btn-twitter:focus,
.btn-twitter:hover {
  outline: 0;
  color: #f4f5f7;
  background-color: #39a9e0 !important;
  border: solid #fff 1px;
}
.btn-dribble:focus,
.btn-dribble:hover {
  outline: 0;
  color: #f4f5f7;
  background-color: #0077b5 !important;
  border: solid #fff 1px;
}
.btn-insta:focus,
.btn-insta:hover {
  outline: 0;
  color: #f4f5f7;
  background: #f09433;
  background: -moz-linear-gradient(
    45deg,
    #f09433 0%,
    #e6683c 25%,
    #dc2743 50%,
    #cc2366 75%,
    #bc1888 100%
  );
  background: -webkit-linear-gradient(
    45deg,
    #f09433 0%,
    #e6683c 25%,
    #dc2743 50%,
    #cc2366 75%,
    #bc1888 100%
  );
  background: linear-gradient(
    45deg,
    #f09433 0%,
    #e6683c 25%,
    #dc2743 50%,
    #cc2366 75%,
    #bc1888 100%
  );
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#f09433', endColorstr='#bc1888',GradientType=1 );
  border: solid #fff 1px;
}
.btn-dribble,
.btn-envelope,
.btn-facebook,
.btn-twitter,
.btn-youtube,
.btn-insta,
.btn-meetup {
  /* -webkit-transition: all 0.3s ease-in-out;
  -moz-transition: all 0.3s ease-in-out;
  -o-transitino: all 0.3s ease-in-out; */
  transition: all 0.7s;
  height: 50px !important;
  width: 50px !important;
  border-radius: 100%;
  font-size: 30px;
  line-height: 37px !important;
  color: dark gray;
}
.btn-youtube:focus,
.btn-youtube:hover {
  outline: 0;
  color: #f4f5f7;
  background-color: #fb1900 !important;
  border: solid #fff 1px;
}
.btn-meetup:hover,
.btn-meetup:focus {
  background-color: #f64060 !important;
  border: solid #fff 1px;
  outline: 0;
  color: #f4f5f7;
}
.btn {
  display: inline-block;
  font-weight: 400;
  /* color: #212529; */
  text-align: center;
  vertical-align: unset;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  background-color: transparent;
  border: 1px solid transparent;
  padding: 0.375rem 0.75rem;
  padding: 0.375rem 0.75rem;
  font-size: 1.5rem;
  line-height: 1.5;
  /* border-radius: 0.25rem; */
  transition: color 0.6s ease-in-out, background-color 0.7s ease-in-out,
    border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}
.title {
  color: ghostwhite;
  font-size: 1.7rem;
  font-weight: 600;
  line-height: 1.125;
}
footer.site-footer {
  color: ghostwhite;
  background-color: #333;
}
img.jsDevLogo {
  width: 1.5%;
  position: absolute;
  margin-left: -26px;
  display: inline-block;
  margin-top: 2px;
}

.jsLink {
  display: inline-block;
  margin-left: 26px;
}
.jsLink a:hover,
.jsLink a:focus {
  color: #27ca8d !important;
  /* text-decoration: underline !important; */
}
.jsLink a {
  text-decoration: none !important;
  transition: 0.7s !important;
  font-size: 15px;
  font-weight: 700;
}
@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  .prefooter img {
    width: 11%;
    padding-top: 5%;
    margin-left: 5%;
  }
  .title {
    color: ghostwhite;
    font-size: 1.2rem;
    font-weight: 600;
    line-height: 1.125;
    /* display: none !important; */
  }
  .prefooter {
    padding: 20px 10px 0px !important;
  }
  ul.social-media {
    padding-top: 0px;
  }
  .social-media li {
    display: inline-block;
    padding: 8px;
  }
  li.footlink {
    display: inline-block;
    padding: 8px;
  }
  footer.site-footer {
    font-size: 14px;
  }
}
</style>
