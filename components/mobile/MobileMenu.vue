<template>
  <section :class="{ 'mobileMenu--open': global.menuOpen }" class="mobileMenu pos--fix z--max inset o--0">
    <!--  -->

    <nav class="mobileMenu__nav flex alignI--center">
      <ul class="mobileMenu__list flex flex--dir-c">
        <li class="mobileMenu__navItem">
          <NuxtLink class="mobileMenu__link pos--rel fs--24 fc--white ff--inter" to="/">About Us</NuxtLink>
        </li>
        <li class="mobileMenu__navItem flex alignI--center">
          <NuxtLink class="mobileMenu__link pos--rel fs--24 fc--white ff--inter" to="/second">Clients</NuxtLink>
          <CaretIcon class="mobileMenu__caret" />
        </li>
         <li class="mobileMenu__navItem flex alignI--center">
          <NuxtLink class="mobileMenu__link pos--rel fs--24 fc--white ff--inter" to="/second">Candidates</NuxtLink>
          <CaretIcon class="mobileMenu__caret" />
        </li>
         <li class="mobileMenu__navItem flex alignI--center">
          <NuxtLink class="mobileMenu__link pos--rel fs--24 fc--white ff--inter" to="/second">Sectors</NuxtLink>
          <CaretIcon class="mobileMenu__caret" />
        </li>
         <li class="mobileMenu__navItem flex alignI--center">
          <NuxtLink class="mobileMenu__link pos--rel fs--24 fc--white ff--inter" to="/second">News</NuxtLink>
        </li>
         <li class="mobileMenu__navItem flex">
          <NuxtLink class="mobileMenu__link pos--rel fs--24 fc--white ff--inter" to="/second">Contact</NuxtLink>
        </li>
      </ul>
    </nav>

    <!--  -->
  </section>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'MobileMenu',
  computed: {
    ...mapState(['global'])
  },
  methods: {
    closeMenu() {
      this.$store.dispatch('global/updateMenuOpen', false)
    }
  }
}
</script>

<style lang="scss">
.mobileMenu {
  display: none;
}
//----------------------------------------//

// 960
@include breakpoint(l) {
  .mobileMenu {
    display: block;
    background: var(--white);
    padding: 40px;
    visibility: hidden;
    transition: visibility 0.2s ease, opacity 0.2s ease;

    &__nav {
      width: 100%;
      height: 100%;
      flex-wrap: nowrap;
    }

    &__navItem {
      list-style: none;
      margin-bottom: 24px;
    }

    &__link {
      color: var(--greenDark);
      &::after {
        position: absolute;
        content: "";
        background: $green;
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

    //
    &--open {
      opacity: 1;
      visibility: visible;
    }
  }
}
</style>
