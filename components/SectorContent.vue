<template>
	<Section class="sectorContent pos--rel">
		<div class="sectorContent__container container container--medium pos--rel flex flex--dir-c alignI--start">
			<div class="sectorContent__headerHolder flex flex--dir-c alignI--center">
				<h3 class="sectorContent__header fs--40 fc--greyDarker fw--600 ff--montserrat lh--125">Our Industry Sectors</h3>
				<p class="sectorContent__text fs--18 fc--greyDark ff--montserrat lh--200">Large Paragragh Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In sagittis felis non pharetra dapibus. Maecenas in laoreet justo, at maximus nibh. Curabitur laoreet egestas dui vitae aliquet. </p>
			</div>
			<div class="sectorContent__grid flex justifyC--between">
				<div v-for="(sector, i) in sectors" :key="sector + i" class="sectorContent__item pos--rel">
					<a :href="sector.link" target="_blank" class="sectorContent__itemLink">
						<div class="sectorContent__imageHolder pos--rel">	
							<img class="sectorContent__image pos--abs" :src="`/images/${sector.image}.jpg`" alt="" />
						</div>
					</a>
          <div class="sectorContent__overlay" :class="'sectorContent__overlay--' + i">
						<h3 class="sectorContent__name fc--white fs--24 fw--600 ff--montserrat lh--120">{{ sector.name }}</h3>
						<a :href="sector.link" target="_blank" class="sectorContent__link flex alignI--center">
            	<p class="sectorContent__label fc--green fs--16 ff--montserrat lh--120">{{ sector.linkLabel }}</p>
							<ArrowIconSmall class="sectorContent__arrow"/>
						</a>
          </div>
			</div>
			</div>
		</div>
	</section>
</template>

<script>
import ArrowIconSmall from '~/assets/svgs/interface/arrow-small.svg?inline'
export default {
	name: 'SectorContent',
	components: {
		ArrowIconSmall
	},
	data() {
    return {
      sectors: [
        {
          image: 'information-technology',
          link: '/',
          name: 'Information Technology',
          linkLabel: 'See jobs in this sector'
        },
				{
          image: 'digital-media',
          link: '/',
          name: 'Digital Media',
          linkLabel: 'See jobs in this sector'
        },
				{
          image: 'it-security',
          link: '/',
          name: 'IT Security',
          linkLabel: 'See jobs in this sector'
        },
				{
          image: 'legal-it',
          link: '/',
          name: 'Legal IT',
          linkLabel: 'See jobs in this sector'
        },
       
			]
		}
	}
}
</script>

<style lang="scss">
.sectorContent {
	background: $white;
	padding: 109px 0 112px;

	&__headerHolder {
		width: 100%;
		margin-bottom: 55px;
	}

	&__grid {
		width: 100%;
	}

	&__header, &__text {
		text-align: center;
	}

	&__header {
		margin-bottom: 30px;
	}

	&__imageHolder {
		width: 100%;
		height: 313px;
		overflow: hidden;
	}


	&__image {
		width: 100%;
		height: 100%;
		object-fit: cover;
		top: 0;
		right: 0;
		bottom: 0;
		left: 0;
		transition: transform 0.8s ease;

	}

	&__overlay {
		width: 100%;
		background-color: $greyDarker;
		background-position: bottom;
		background-repeat: none;
		background-blend-mode: multiply;
		padding: 22px 21px 20px;
		left: 0;
		bottom: 0;
		position: absolute;

		&--0 {
			background-image: url('static/images/information-technology.jpg');
		}

		&--1 {
			background-image: url('static/images/digital-media.jpg');
		}
		&--2 {
			background-image: url('static/images/it-security.jpg');
		}
		&--3 {
			background-image: url('static/images/legal-it.jpg');
		}
	}

	&__text {
		line-height: 36px;
		max-width: 920px;
	}

	&__label {
		margin-right: 10px;
	}

	&__link {
		&:hover {
			.sectorContent__arrow {
				transform: translateX(4px);
			}
		}
	}

	&__arrow {
		transition: transform 0.3s ease;
	}

	&__item {
		width: calc(50% - 30px);
		margin-right: 30px;
		margin-bottom: 44px;

		&:nth-child(n + 3) {
			margin-bottom: 0;
		}

		&:nth-child(2), &:nth-child(4) {
			margin-right: 0;
			width: 50%;
		}

		&:hover {
			cursor: pointer;
			.sectorContent__image {
				transform: scale(1.05);
			}
		}
	}
}

//---------------------------------------//
// 600
@include breakpoint(s) {
	.sectorContent {
		padding: 54px 0 56px;

		&__headerHolder {
			margin-bottom: 27.5px;
		}


			&__header {
				font-size: 32px;
			}

			&__text {
				font-size: 16px;
			}

			&__name {
				font-size: 22px;
			}


			&__item {
				width: 100%;
				margin-right:0;
				margin-bottom: 22px;


				&:nth-child(n + 3) {
					margin-bottom: 22px;
				}

				&:nth-last-child(1) {
					margin-bottom: 0;
				}
			}
		}
}
</style>
