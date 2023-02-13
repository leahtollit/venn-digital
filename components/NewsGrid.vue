<template>
  <Section class="newsGrid">
		<div class="newsGrid__container container container--medium pos--rel flex">
			<div class="newsGrid__headerHolder flex justifyC--between alignI--center">
				<h3 class="newsGrid__header fs--40 fc--black fw--600">Latest News &amp; Articles</h3>
				<BaseBtn class="baseBtn baseBtn--green" :to="'/'">All News</BaseBtn>
			</div>
			<div class="newsGrid__grid grid">
				<div v-for="(el, i) in items" :key="el + i" class="newsGrid__itemHolder" :class="'newsGrid__itemHolder--' + i">
          <div class="newsGrid__body flex alignI--center">
            <div v-if="el.hasImage === true" class="newsGrid__imgHolder pos--rel" :class="'newsGrid__imgHolder--' + i">
              <img class="newsGrid__img pos--abs" :src="el.image" alt="" />
            </div>
						<div class="newsGrid__content pos--rel">
							<div class="newsGrid__copyHolder flex flex--dir-c">
								<p class="newsGrid__title ff--inter fw--700 fs--22 fc--black pos--rel">{{ el.title }}</p>
								<p class="newsGrid__text ff--inter fs--16 fc--black pos--rel o--8">
									{{ el.text }}
								</p>
							</div>
							<BaseBtn class="baseBtn baseBtn--green" :link="el.buttonLink">{{ el.buttonLabel }} </BaseBtn>
						</div>
          </div>
				</div>
			</div>
		</div>
  </section>
</template>

<script>
export default {
  name: 'NewsGrid',
	data() {
    return {
      items: [
        {
          image: '/images/article-image-one.jpg',
          title: 'Gravida veroeros',
          text: 'Feugiat ultrices sed nibh. Quisque a lectus. Donec consectetuer ligula vulputate sem tristique cursus. Lorem nulla sed gravida non magna.',
					buttonLabel: 'Read More',
					buttonLink: '/',
					hasImage: true
        },
        {
          title: 'Gravida veroeros',
          text: 'Feugiat ultrices sed nibh. Quisque a lectus. Donec consectetuer ligula vulputate sem tristique cursus. Lorem nulla sed gravida non magna.',
					buttonLabel: 'Read More',
					buttonLink: '/',
					hasImage: false
        },
        {
          title: 'Gravida veroeros',
          text: ' Feugiat ultrices sed nibh. Quisque a lectus. Donec consectetuer ligula vulputate sem tristique cursus. Lorem nulla sed gravida non magna.',
					buttonLabel: 'Read More',
					buttonLink: '/',
					hasImage: false
        },
				{
          image: '/images/article-image-two.jpg',
          title: 'Gravida veroeros',
          text: ' Feugiat ultrices sed nibh. Quisque a lectus. Donec consectetuer ligula vulputate sem tristique cursus. Lorem nulla sed gravida non magna.',
					buttonLabel: 'Read More',
					buttonLink: '/',
					hasImage: true
        },
				{
          image: '/images/article-image-three.jpg',
          title: 'Gravida veroeros',
          text: ' Feugiat ultrices sed nibh. Quisque a lectus. Donec consectetuer ligula vulputate sem tristique cursus. Lorem nulla sed gravida non magna.',
					buttonLabel: 'Read More',
					buttonLink: '/',
					hasImage: true
        }
			]
		}
	}
		
}
</script>

<style lang="scss">
.newsGrid {
	padding: 198px 0 0;

	&__headerHolder {
		width: 100%;
		margin-bottom: 82px;
	}

	&__grid {
	  column-gap: 30px;
		width: 100%;
  	row-gap: 30px;
		grid-template-columns: auto auto auto;
		grid-template-areas: 
			"article-one article-two article-five"
			"article-one article-four article-five"
			"article-three article-four article-five";
	}
	
	&__itemHolder {
		max-width: 350px;
		width: 100%;

		&--0 {
			grid-area: article-one;
		}

		&--1 {
			grid-area: article-two;
		}

		&--2 {
			grid-area: article-three;
		}

		&--3 {
			grid-area: article-four;
		}

		&--4 {
			grid-area: article-five;
		}
	}

	&__imgHolder {
		width: 100%;
		height: 100%;

		&--0 {
			padding-bottom: 72%;
		}

		&--3 {
			padding-bottom: 68%;
		}

		&--4 {
			padding-bottom:  123%;
		}

	}

	&__img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	&__title {
		margin-bottom: 13px;
	}


	&__copyHolder {
		padding-bottom: 42px;
	}

	&__content {
		background: $white;
		padding: 36px 30px 45px 29px;
	}
	
}

//----------------------------------------//
// 960
@include breakpoint(l) {
  .newsGrid {
		&__grid {
			grid-template-columns: auto auto;
			column-gap: 30px;
			grid-template-areas: 
			"article-one article-two"
			"article-one article-three"
			"article-five article-four";
		}

		&__itemHolder {
			max-width: 100%;
		}
	}
}

//----------------------------------------//
// 600
@include breakpoint(s) {
  .newsGrid {
		padding: 99px 0 0;

		&__headerHolder {
			margin-bottom: 41px;
		}

		&__header {
			font-size: 32px;
			margin-bottom: 18px;
		}
		&__grid {
			grid-template-columns: auto;
			column-gap: 0;
			grid-template-areas: 
			"article-one"
			"article-two"
			"article-three" 
			"article-four"
			"article-five";
		}

		&__itemHolder {
			max-width: 100%;
		}

		&__imgHolder {
			height: 350px;

			&--0, &--3, &--4 {
				padding-bottom: 0;
			}
		}
	}
}
</style>
