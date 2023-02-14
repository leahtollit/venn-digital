<template>
  <div v-if="parentLink" :class="'baseBtn--' + type" class="baseBtn pos--rel ta--center buttonReset">
    <p v-if="!loading" class="baseBtn__label lh--150 fs--16 ff--inter fw--700"><slot /></p>
    <div v-else class="baseLoader baseLoader--small" />
  </div>

  <NuxtLink
    v-else-if="link && !external"
    :to="link"
    :class="'baseBtn--' + type"
    class="baseBtn pos--rel ta--center buttonReset">
    <p v-if="!loading" class="baseBtn__label lh--150 fs--16 ff--inter fw--700"><slot /></p>
    <div v-else class="baseLoader baseLoader--small" />
  </NuxtLink>

  <a
    v-else-if="link && external"
    :href="link"
    :class="'baseBtn--' + type"
    class="baseBtn pos--rel ta--center buttonReset"
    target="_blank">
    <p v-if="!loading" class="baseBtn__label lh--150 fs--16 ff--inter fw--700"><slot /></p>
    <div v-else class="baseLoader baseLoader--small" />
  </a>

  <button v-else :class="'baseBtn--' + type" class="baseBtn pos--rel ta--center buttonReset">
    <p v-if="!loading" class="baseBtn__label lh--150 fs--16 ff--inter fw--700"><slot /></p>
    <div v-else class="baseLoader baseLoader--small" />
  </button>
</template>

<script>
export default {
  name: 'BaseBtn',
  props: {
    type: {
      type: String,
      default: 'btn',
      validator(value) {
        return ['btn', 'link'].includes(value) // The value must match one of these strings
      }
    },
    link: {
      type: String,
      default: ''
    },
    external: {
      type: Boolean,
      default: false
    },
    parentLink: {
      type: Boolean,
      default: false
    },
    loading: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss">
.baseBtn {
  position: relative;
  overflow: hidden;
  display: inline-block;

  &:after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 101%;
    height: 100%;
    background: $white;
    transform: translateY(100%);
    transition: transform .3s ease;
    z-index: 0;
  }
  // button styles
  &--white {
    border: 2px solid $white;
    padding: 14px 59px;

    &:after {
      background: $white;
    }


    .baseBtn__label {
      color: $white;
    }

    &:hover {
      &:after {
        transform: translateY(0)
      }

      .baseBtn__label {
        color: $greenDark;
      }
    }
  }

  &--green {
    border: 2px solid $green;
    padding: 14px 59px;

    .baseBtn__label {
      color: $greenDark;
    }

    &:after {
      background: $green;
    }

    &:hover {
      &:after {
        transform: translateY(0)
      }

      .baseBtn__label {
        color: $white;
      }
    }

  }



  &--btn:hover,
  &__parentLink:hover .baseBtn--btn {

  }

  // link styles
  &--link {
    
  }

  //
  &--link:hover,
  &__parentLink:hover .baseBtn--link {
    border-bottom: 1px solid rgba(var(--rgb-black), 1);
  }

  &__label {
    line-height: 24px;
    transition: color 0.3s ease;
    z-index: 2;
    position: relative;
  }
}
</style>
