<template>
  <div>
    <!-- eslint-disable -->
    <nav
      class="navbar has-shadow is-fixed-top"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <nuxt-link class="navbar-item" to="/">
          <site-logo v-if="$siteConfig.logo === 'logo-component'" />
          <img
            v-else
            :src="$siteConfig.logo"
            :alt="$siteConfig.siteName"
            class="logo"
          />
        </nuxt-link>

        <hamburger-button @click="active = !active" />
      </div>

      <div
        :class="{
          'navbar-menu': true,
          'is-active': active
        }"
      >
        <ul class="navbar-end">
          <li>
            <nuxt-link class="navbar-item navDrop1" to="/">Home</nuxt-link>
          </li>
          <li>
            <div class="dropdown about is-right">
              <div class="dropdown-trigger">
                <button
                  id="navDrop"
                  class="button dropdown navDrop1"
                  aria-haspopup="true"
                  aria-controls="dropdown-menu"
                  @click="myFilter1()"
                >
                  <span>About</span>
                  <span class="icon is-small">
                    <font-awesome-icon
                      :icon="{ prefix: 'fas', iconName: 'angle-down' }"
                    />
                  </span>
                </button>
              </div>
              <div
                id="dropdown-menu"
                class="dropdown-menu animated zoomIn"
                role="menu"
              >
                <div class="dropdown-content" @click="myFilter1()">
                  <nuxt-link class="navbar-item" to="/about"
                    >Our People</nuxt-link
                  >
                  <hr class="dropdown-divider" />
                  <nuxt-link class="navbar-item" to="/infinite"
                    >What We Do</nuxt-link
                  >
                </div>
              </div>
            </div>
          </li>
          <li
            v-for="item in $siteConfig.mainMenu"
            :key="item.link"
            class="navbar-item"
            @click="active = false"
          >
            <component
              :is="item.link.startsWith('http') ? 'a' : 'nuxt-link'"
              :href="item.link"
              :to="item.link"
              :target="item.target ? item.target : '_self'"
              >{{ item.name }}</component
            >
          </li>
          <li>
            <div class="dropdown blog is-right">
              <div class="dropdown-trigger">
                <button
                  id="navDrop2"
                  class="button dropdown"
                  aria-haspopup="true"
                  aria-controls="dropdown-menu"
                  @click="myFilter()"
                >
                  <span>Blog Talk</span>
                  <span class="icon is-small">
                    <font-awesome-icon
                      :icon="{ prefix: 'fas', iconName: 'angle-down' }"
                    />
                  </span>
                </button>
              </div>
              <div
                id="dropdown-menu"
                class="dropdown-menu animated zoomIn"
                role="menu"
              >
                <div class="dropdown-content" @click="myFilter()">
                  <nuxt-link class="navbar-item" to="/blog"
                    >Blog Posts</nuxt-link
                  >
                  <hr class="dropdown-divider" />
                  <nuxt-link class="navbar-item" to="/categories"
                    >Categories</nuxt-link
                  >
                </div>
              </div>
            </div>
          </li>
          <li class="navbar-item site-search-wrapper">
            <site-search />
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>
<script>
import SiteSearch from '~/components/SiteSearch'
import HamburgerButton from '~/components/HamburgerButton'
import 'bulma/css/bulma.css'
export default {
  name: 'SiteNav',
  components: { SiteSearch, HamburgerButton },
  data() {
    return {
      active: false
    }
  },
  methods: {
    myFilter() {
      const dropdown = document.querySelector('.dropdown.blog')
      dropdown.classList.toggle('is-active')
    },
    myFilter1() {
      const dropdown = document.querySelector('.dropdown.about')
      dropdown.classList.toggle('is-active')
    },
    dropdownContent() {
      const dropdown = document.querySelector('.dropdown.is-active')
      dropdown.removeClass('is-active')
    }
  }
}
</script>
<style lang="scss" scoped>
button.navDrop1 {
  margin-top: 0.5rem !important;
}
a.navDrop1 {
  margin-top: 0.4rem !important;
}
a.navDrop1:hover {
  color: #faa146;
  background-color: transparent;
}
.navbar-end button.dropdown:hover {
  color: #f8ab44;
}
.dropdown .navbar-item {
  transition: 0.3s;
}
.dropdown .navbar-item:hover {
  background-color: transparent;
  color: #faa146;
  border: 1px solid #faa146;
}
#navDrop.dropdown,
#navDrop2.dropdown {
  margin-left: 0%;
  margin-top: 7%;
  background-color: transparent;
  border-color: transparent;
  transition: 0.7s ease-in-out;
}
button#navDrop.dropdown:hover button#navDrop2.dropdown:hover {
  background-color: #363636;
  color: whitesmoke;
}
.dropdown-menu.animated.zoomIn {
  animation-duration: 300ms;
}
.navbar-item img {
  max-height: 4.75rem;
}
.vue-skip-to:focus {
  background-color: #fff;
  left: 0;
  color: #363636;
  border: solid #363636 1px;
}
.site-search-wrapper {
  transform: translateX(5px);
  @media (max-width: 1023px) {
    display: none;
  }
}
</style>
