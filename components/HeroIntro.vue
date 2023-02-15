<template>
  <Section class="heroIntro ">
		<div class="heroIntro__container container container--medium pos--rel flex flex--dir-c alignI--start justifyC--center z--1">
		
			<div class="heroIntro__contentHolder pos--rel flex justifyC--start flex--dir-c z--2">
				<h1 class="heroIntro__header fc--white fs--40 ff--montserrat fw--600 lh--125">All the answers under one roof</h1>
				<p class="heroIntro__text fc--white fs--24 ff--montserrat fw--400 lh--150">IT and Tech Recruitment for everything from start ups to large enterprises</p>
			</div>
			<BaseBtn class="baseBtn--green">Read More </BaseBtn>
			<div class="heroIntro__nav flex flex--dir-c pos--abs y--center ">
				<div
        class="heroIntro__point"
        :class="{ 'heroIntro__point--active': currentSlide === 0 }"
        @click="selectSlide(0)" />
      <div
        class="heroIntro__point"
        :class="{ 'heroIntro__point--active': currentSlide === 1 }"
        @click="selectSlide(1)" />
      <div
        class="heroIntro__point"
        :class="{ 'heroIntro__point--active': currentSlide === 2 }"
        @click="selectSlide(2)" />
			</div>
		</div>
		<div
          v-for="(el, i) in children"
          :key="el + i"
          class="heroIntro__imageHolder pos--abs"
          :class="{ 'heroIntro__imageHolder--active': currentSlide === i }">
					<img class="heroIntro__image pos--abs" :src="el.image">
	</div>
  </section>
</template>

<script>
export default {
  name: 'HeroIntro',
	data() {
    return {
      currentSlide: 0,
			intervalID: null,
			children: [
				{
          image: '/images/hero-image.jpg',
        },
				{
          image: '/images/jellyfish-image-two.jpg',
        },
				{
          image: '/images/jellyfish-image-three.jpg',
        },

		]
    }
  },
	methods: {
    setupInterval() {
      if (this.intervalID === null) {
        this.intervalID = setInterval(() => {
          this.currentSlide++
          if (this.currentSlide === this.children.length) {
            this.currentSlide = 0
          }
        }, 4000)
      }
    },
		selectSlide(slide) {
      this.currentSlide = slide
      clearInterval(this.intervalID)
      this.intervalID = null
    }
	}
}
</script>

<style lang="scss">
.heroIntro {
	width: 100%;
	height: 100vh;

	&__imageHolder {
		width: 100vw;
		height: 100vh;
		top: 0;
		left: 0;
		opacity: 0;
    transition: opacity 0.6s;

    &--active {
      opacity: 1;
    }
	}

	&__image {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}


	&__container {
		padding-top: 288px;
		padding-bottom: 131px;
		height: 100%;
	}


	&__header {
		max-width: 634px;
	}

	&__header, &__text  {
		margin-bottom: 25px;
		width: 100%;
	}

	&__text {
		max-width: 543px;
	}

	&__nav {
		right: 7%;
	}
	&__point {
		width: 15px;
		height: 15px;
		background: $green;
		opacity: 0.3;
		border-radius: 50%;
		margin-bottom: 6px;
		transition: opacity .3s ease;

		&--active {
      opacity: 1;
    }

		&:nth-last-child(1) {
			margin-bottom: 0;
		}

		&:hover {
			cursor: pointer;
			opacity: 1;
		}
	}
	
}

// This media query targets screens shorter than 810px but wider than 750px to make things taller/reduce margins
@media screen and (min-width: 750px) and (max-width: 1920px) and (max-height: 810px) {
	.heroIntro {
		&__container {
      padding-top: 144px;
		padding-bottom: 0;
		}
	}
}

//----------------------------------------//
// 1080
@include breakpoint(xl) {
  .heroIntro {

		&__container {
			padding-top: 144px;
			padding-bottom: 100px;
			justify-content: end;
		}

		&__header {
			font-size: 38px;
		}

		&__nav {
			right: 4%;
		}
	}
}
</style>
