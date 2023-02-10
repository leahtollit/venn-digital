<template>
  <header class="globalHeader pos--fix z--max" :class="{ 'globalHeader--collapsed': collapsed }">
    <div class="globalHeader__container container container--medium flex alignI--start justifyC--between">
      <NuxtLink to="/" class="globalHeader__logo"><GlobalLogo class="globalHeader__logoImage" /></NuxtLink>
      <ul class="globalHeader__nav flex">
        <li class="globalHeader__navItem flex">
          <NuxtLink class="globalHeader__link pos--rel fs--16 fc--white ff--inter" to="/">About Us</NuxtLink>
        </li>
        <li class="globalHeader__navItem flex alignI--center">
          <NuxtLink class="globalHeader__link pos--rel fs--16 fc--white ff--inter" to="/second">Clients</NuxtLink>
          <CaretIcon class="globalHeader__caret" />
        </li>
         <li class="globalHeader__navItem flex alignI--center">
          <NuxtLink class="globalHeader__link pos--rel fs--16 fc--white ff--inter" to="/second">Candidates</NuxtLink>
          <CaretIcon class="globalHeader__caret" />
        </li>
         <li class="globalHeader__navItem flex alignI--center">
          <NuxtLink class="globalHeader__link pos--rel fs--16 fc--white ff--inter" to="/second">Sectors</NuxtLink>
          <CaretIcon class="globalHeader__caret" />
        </li>
         <li class="globalHeader__navItem flex alignI--center">
          <NuxtLink class="globalHeader__link pos--rel fs--16 fc--white ff--inter" to="/second">News</NuxtLink>
        </li>
         <li class="globalHeader__navItem flex">
          <NuxtLink class="globalHeader__link pos--rel fs--16 fc--white ff--inter" to="/second">Contact</NuxtLink>
        </li>
      </ul>
      <SearchIcon class="globalHeader__searchIcon" />
    </div>
  </header>
</template>

<script>
import GlobalLogo from '~/assets/svgs/interface/global-logo.svg?inline'
import CaretIcon from '~/assets/svgs/interface/caret-down-solid.svg?inline'
import SearchIcon from '~/assets/svgs/interface/search-solid.svg?inline'


export default {
  name: 'GlobalHeader',
  components: {
    GlobalLogo,
    CaretIcon,
    SearchIcon
  },
  data() {
    return {
      collapsed: false
    }
  },
  mounted() {
    window.addEventListener('scroll', () => {
      if (window.scrollY > 10) {
        this.collapsed = true
      } else {
        this.collapsed = false
      }
    })
  },
  methods: {
    scrollToElement(element) {
      const offset = document.querySelector(element).offsetTop
      const headerHeight = document.querySelector('.globalHeader').clientHeight

      window.scrollTo({
        top: offset - headerHeight,
        behavior: 'smooth'
      })
    }
  }
}
</script>

<style lang="scss">
.globalHeader {
  padding: 46px 0;
  margin: 0;
  background: none;
  top: 0;
  right: 0;
  left: 0;
  transition: padding 0.3s ease, opacity 0.3s ease, background 0.3s ease;

  &--collapsed {
    padding: 23px 0;
    background: $greenDark;
  }


  &__logoImage {
    width: 121.9px;
    height: 36.75px;
  }

  &__nav {
    padding: 0;
  }

  &__navItem {
    margin-right: 32px;

    &:nth-last-child(1) {
      margin-right: 0;
    }
  }

  &__link {
    &::after {
      position: absolute;
      content: "";
      background: $white;
      width: 100%;
      height: 1px;
      bottom: -0.1875rem;
      left: 0;
      transform: scaleX(0);
      transition: transform .7s cubic-bezier(0.25, 0.1, 0.25, 1);
    }

    &:hover {
      &::after {
        transform: scaleX(1);
      }
    }
  }

  &__caret {
    width: 8.81px;
    height: 5px;
    margin-left: 18px;
  }

  &__searchIcon {
    width: 19px;
    height: 19px;
  }
}

//----------------------------------------//

// 1080
@include breakpoint(xl) {
  .globalHeader {

    &__link {
      font-size: 14px;    
    }


    &__navItem {
      margin-right: 16px;
    }
  }
}


//----------------------------------------//
// 600
@include breakpoint(s) {
  .globalHeader {


    &__nav {
      display: none;
    }
  }
}
</style>
