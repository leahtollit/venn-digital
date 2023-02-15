<template>
    <div class="sliderCarousel pos--rel">
      <div ref="slider" class="sliderCarousel__slider keen-slider flex pos--rel">
        <div v-for="(client, i) in clients" :key="client + i" class="sliderCarousel__slide keen-slider__slide pos--rel grid placeI--center">
          <div class="sliderCarousel__imgHolder pos--rel" :class="'sliderCarousel__imgHolder--' + client.client" >
						<img :src="client.image" alt="" class="sliderCarousel__img pos--abs">
					</div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  // https://keen-slider.io/docs
  import KeenSlider from 'keen-slider'
  import 'keen-slider/keen-slider.min.css'
  
  export default {
    name: 'SliderCarousel',
    data() {
      return {
        current: 0,
        slider: null,
				clients: [
					{
						client: '1',
						image: '/images/logo-one.png'
					},
					{
						client: '2',
						image: 'images/logo-two.png'
					},
					{
						client: '3',
						image: '/images/logo-three.png'
					},
					{
						client: '4',
						image: '/images/logo-four.png'
					},
					{
						client: '1',
						image: '/images/logo-one.png'
					},
					{
						client: '2',
						image: '/images/logo-two.png'
					},
					{
						client: '3',
						image: '/images/logo-three.png'
					},
					{
						client: '4',
						image: '/images/logo-four.png'
					},
					{
						client: '1',
						image: '/images/logo-one.png'
					},
					{
						client: '2',
						image: '/images/logo-two.png'
					},
					{
						client: '3',
						image: '/images/logo-three.png'
					},
					{
						client: '4',
						image: '/images/logo-four.png'
					}
			  ]
      }
    },
    mounted() {
      this.slider = new KeenSlider(this.$refs.slider, {
        selector: '.sliderCarousel__slide',
        initial: this.current,
        slideChanged: (s) => {
          this.current = s.track.details.rel
        },
				slides: {
          spacing: 20,
					perView: 15
        },
        loop: true,
				breakpoints: {
					'(max-width: 1920px)': {
          	slides: {
							spacing: 20,
							perView: 10
          	}
					},
					'(max-width: 1400px)': {
          	slides: {
							spacing: 20,
							perView: 6
          	}
					},
        '(max-width: 1200px)': {
          slides: {
            perView: 6,
            spacing: 20
          }
        },
				'(max-width: 960px)': {
          slides: {
            perView: 4,
            spacing: 15
        
          }
				},
        '(max-width: 750px)': {
          slides: {
            perView: 3,
            spacing: 15
        
          }
        },
        '(max-width: 500px)': {
          slides: {
            perView: 2,
            spacing: 10
         
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
  .sliderCarousel {
		width: 300%;
		overflow: visible;
    //
		&__slider {
    flex-wrap: nowrap;
    align-content: flex-start;
    overflow: visible !important;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-touch-callout: none;
    -khtml-user-select: none;
    touch-action: pan-y;
    -webkit-tap-highlight-color: transparent;
    width: 100%;
  }

  &__slide {
    overflow: hidden;
    width: 100%;
    background: var(--white);
    height: 160px;

  }
		&__imgHolder {
			&--1 {
				width: 167px;
				height: 126px;
			}

			&--2 {
				width: 142px;
				height: 80px;
			}

			&--3 {
				width: 84px;
				height: 84px;
			}

			&--4 {
				width: 159px;
				height: 90px;
			}
		}

		&__img {
			width: 100%;
			height: 100%;
			object-fit: contain;
		}
  
  }

//----------------------------------------//
// 1920
@include breakpoint(sssl) {
  .sliderCarousel {
		width: 200%;
	}
}

	//----------------------------------------//
// 1400
@include breakpoint(sl) {
  .sliderCarousel {
		width: 100%;
	}
}
  </style>

  