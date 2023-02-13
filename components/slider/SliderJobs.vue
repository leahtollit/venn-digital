<template>
    <div class="sliderJobs pos--rel">
      <div ref="slider" class="sliderJobs__slider keen-slider flex pos--rel">
        <div v-for="(slide, i) in slides" :key="slide + i" class="sliderJobs__slide keen-slider__slide">
        <div class="sliderJobs__roleHeader">
            <p class="sliderJobs__role fc--white fs--18"> {{ slide.role }}</p>
        </div>
        <div class="sliderJobs__body flex flex--dir-c">
          <div class="sliderJobs__row flex">
            <SalaryIcon class="sliderJobs__icon sliderJobs__icon--salary"/>
            <p class="sliderJobs__salary fs--14 fc--greyLight "> {{ slide.salary }} </p>
          </div>
          <div class="sliderJobs__row flex">
            <LocationIcon class="sliderJobs__icon sliderJobs__icon--location"/>
            <p class="sliderJobs__location fs--14 fc--greyLight"> {{ slide.location }} </p>
          </div>
          <div class="sliderJobs__row flex">
            <ClockIcon class="sliderJobs__icon sliderJobs__icon--clock"/>
            <p class="sliderJobs__type fs--14 fc--greyLight"> {{ slide.type }} </p>
          </div>
            <p class="sliderJobs__description fs--16 fc--greyLight"> {{ slide.description }} </p>
						<NuxtLink class="sliderJobs__link flex alignI--center" :to="slide.link">
							<p class="sliderJobs__linkLabel fc--green"> {{slide.linkLabel}}</p>
							<ArrowIcon class="sliderJobs__arrow"/>
							</Nuxtlink>
        </div> 
      </div>
      </div>

  
      <div class="sliderJobs__btns flex justifyC--end">
        <button
          :class="{ 'sliderJobs__btn--disabled': current === 0 }"
          class="sliderJobs__btn sliderJobs__btn--prev"
          @click="slider.prev()">
          <IconPrev/>
        </button>
  
        <button
          v-if="slider"
          :class="{ 'sliderJobs__btn--disabled': current === slider.track.details.slides.length - 1 }"
          class="sliderJobs__btn sliderJobs__btn--next"
          @click="slider.next()">
          <IconNext/>
        </button>
      </div>
    </div>
  </template>
  
  <script>
  // https://keen-slider.io/docs
  import KeenSlider from 'keen-slider'
  import 'keen-slider/keen-slider.min.css'

	import ArrowIcon from '~/assets/svgs/interface/link-arrow.svg?inline'
	import IconPrev from '~/assets/svgs/interface/prev.svg?inline'
	import IconNext from '~/assets/svgs/interface/next.svg?inline'
  import SalaryIcon from '~/assets/svgs/interface/salary-icon.svg?inline'
  import LocationIcon from '~/assets/svgs/interface/location-icon.svg?inline'
  import ClockIcon from '~/assets/svgs/interface/clock-icon.svg?inline'

  
  export default {
    name: 'SliderBase',
		components: {
			ArrowIcon,
			IconPrev,
			IconNext,
      SalaryIcon,
      LocationIcon,
      ClockIcon
		},
    data() {
      return {
        current: 0,
        slider: null,
        slides: [
        {
          role: 'Electrical Conductor Researcher',
          salary: '£31,000 - £43,000',
          location: 'Germany',
          type: 'Permanent',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In sagittis felis non pharetra dapibus…',
          linkLabel: 'View Job',
          link: '/'
        },
        {
          role: 'Electrical Conductor Researcher',
          salary: '£31,000 - £43,000',
          location: 'Germany',
          type: 'Permanent',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In sagittis felis non pharetra dapibus…',
          linkLabel: 'View Job',
          link: '/'
        },
        {
          role: 'Electrical Conductor Researcher',
          salary: '£31,000 - £43,000',
          location: 'Germany',
          type: 'Permanent',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In sagittis felis non pharetra dapibus…',
          linkLabel: 'View Job',
          link: '/'
        },
        {
          role: 'Electrical Conductor Researcher',
          salary: '£31,000 - £43,000',
          location: 'Germany',
          type: 'Permanent',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In sagittis felis non pharetra dapibus…',
          linkLabel: 'View Job',
          link: '/'
        },
        {
          role: 'Electrical Conductor Researcher',
          salary: '£31,000 - £43,000',
          location: 'Germany',
          type: 'Permanent',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In sagittis felis non pharetra dapibus…',
          linkLabel: 'View Job',
          link: '/'
        },
        {
          role: 'Electrical Conductor Researcher',
          salary: '£31,000 - £43,000',
          location: 'Germany',
          type: 'Permanent',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In sagittis felis non pharetra dapibus…',
          linkLabel: 'View Job',
          link: '/'
        }
      ]
      }
    },
    mounted() {
      this.slider = new KeenSlider(this.$refs.slider, {
        selector: '.sliderJobs__slide',
        initial: this.current,
        slideChanged: (s) => {
          this.current = s.track.details.rel
        },
				slides: {
          perView: 3,
          spacing: 29
        },
        loop: true,
      breakpoints: {
        '(max-width: 1400px)': {
          slides: {
            perView: 3,
            spacing: 29
        
          }
        },
        '(max-width: 1200px)': {
          slides: {
            perView: 3,
            spacing: 29
        
          }
        },
        '(max-width: 750px)': {
          slides: {
            perView: 2,
            spacing: 15
        
          }
        },
        '(max-width: 600px)': {
          slides: {
            perView: 1,
            spacing: 15
         
          }
        }
      }
      })
    },
    destroy() {
      if (this.slider) this.slider.destroy()
    }
  }
  </script>
  
  <style lang="scss">
  .sliderJobs {
		overflow: visible;

    //
    &__slider {
      flex-wrap: nowrap;
      align-content: flex-start;
      -webkit-user-select: none;
      -moz-user-select: none;
      -ms-user-select: none;
      user-select: none;
      -webkit-touch-callout: none;
      -khtml-user-select: none;
      touch-action: pan-y;
      -webkit-tap-highlight-color: transparent;
      width: 100%;
    	max-width: 100vw;
			overflow: visible;
    }
  
    &__slide {
      overflow: hidden;
      height: 369px;
			max-width: 350px;
    }

  
    //

    &__btns {
      margin-top: 30px;
      // right: 0;
    }

    &__btn {
      cursor: pointer;
			background: none;
			border: none;

      &--disabled {
        opacity: 0.5;
        pointer-events: none;
      }

			&--prev {
				margin-right: 68.8px;
			}
    }

    &__roleHeader {
			background: $green;
			padding: 18px 28px 13px 31px;
			border: 2px solid $white;
			border-bottom: none;
		}

		&__body {
			background: $white;
			padding: 15px 29px 30.6px 31px;
			// max-width: 290px;
			width: 100%;
		}

		&__salary {
			margin-bottom: 17.6px;
		}

		&__location {
			margin-bottom: 18px;
		}

		&__type {
			margin-bottom: 20.4px;
		}

		&__description {
			margin-bottom: 18.4px;
			line-height: 24px;
		}

		&__linkLabel {
			margin-right: 15.9px;
		}

		&__link {
			&:hover {
				.sliderJobs__arrow {
					transform: translateX(4px);
				}
			}
		}

		&__arrow {
			transition: transform 0.3s ease;
		}
    
    &__icon {
      &--salary {
      margin-right: 6.2px;
      }

      &--location {
        margin-right: 16px;
      }

      &--clock {
        margin-right: 11.9px;
      }
    }
  }

  //----------------------------------------//
// 750
@include breakpoint(m) {
  .sliderJobs {
    width: 100%;
  

    &__slide {
			height: 100%;
    }

    &__btn--prev {
      margin-right: 34px;
    }
  }
}
  </style>
  