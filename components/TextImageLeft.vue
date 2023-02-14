<template>
  <Section class="textImageLeft pos--rel">
		<div class="textImageLeft__container container container--medium pos--rel flex alignI--start">
			<div class="textImageLeft__imageHolder pos--rel">
				<img src="/images/public-sectors.jpg" alt="" class="textImageLeft__image pos--abs" />
			</div>
			<div class="textImageLeft__contentHolder flex flex--dir-c ">
				<h3 class="textImageLeft__header fs--40 fc--greyDark ff--montserrat lh--120 fw--600">Public Sector</h3>
				<p class="textImageLeft__text ff--inter fs--16 fc--greyLight lh--150 fw--400">Paragragh Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In sagittis felis non pharetra dapibus. Maecenas in laoreet justo, at maximus nibh. Curabitur laoreet egestas dui vitae aliquet. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Curabitur vestibulum ex ut sagittis scelerisque. Integer iaculis, mi at <a class="textImageLeft__textLink fw--700 pos--rel" href="" target="_blank">feugiat tempus</a>, diam risus pellentesque </p>
				<ul class="textImageLeft__list flex flex--dir-c">
					<li class="textImageLeft__listItem flex alignI--center">
						<ArrowIconSmall class="textImageLeft__arrow"/>
						<p class="textImageLeft__listText fs--16 fc--greyLight ff--inter">List element</p>
					</li>
					<li class="textImageLeft__listItem flex alignI--center">
						<ArrowIconSmall class="textImageLeft__arrow"/>
						<p class="textImageLeft__listText fs--16 fc--greyLight ff--inter">List element</p>
					</li>
					<li class="textImageLeft__listItem flex alignI--center">
						<ArrowIconSmall class="textImageLeft__arrow"/>
						<p class="textImageLeft__listText fs--16 fc--greyLight ff--inter">List element</p>
					</li>
				</ul>
				<BaseBtn class="baseBtn baseBtn--green" :link="'/'">Read More</BaseBtn>
			</div>
		</div>
  </section>
</template>

<script>
import ArrowIconSmall from '~/assets/svgs/interface/arrow-small.svg?inline'

export default {
  name: 'TextImageLeft',
	components: {
		ArrowIconSmall
	}
}
</script>

<style lang="scss">
.textImageLeft {
	background: $white;
	padding: 0 0 189px;

	&__header {
		margin-bottom: 30px;
		width: 100%;
	}

	&__contentHolder {
		width: 50%;
	}

	&__text {
		max-width: 540px;
		margin-bottom: 10px;
	}

	&__textLink {
		color: $green;

		&::after {
      position: absolute;
      content: "";
      background: $green;
      width: 100%;
      height: 1px;
      bottom: 0;
      left: 0;
      transform: scaleX(1);
      transition: transform .7s cubic-bezier(0.25, 0.1, 0.25, 1);
    }

    &:hover {
      &::after {
        transform: scaleX(0);
      }
    }
	}

	&__imageHolder {
		width: calc(50% - 30px);
		margin-right: 30px;
		padding-bottom: 38%;
	}

	&__image {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	&__list {
		padding: 0;
		margin-bottom: 22px;
	}

	&__listItem {
		margin-bottom: 10px;

		&:nth-last-child(1) {
			margin-bottom: 0;
		}
	}

	&__arrow {
		margin-right: 10.3px;
	}
	
}

  //----------------------------------------//
// 600
@include breakpoint(s) {
  .textImageLeft {
		padding: 53px 0;

		&__imageHolder {
			width: 100%;
			padding-bottom: 0;
			aspect-ratio: 1 / 1;
			margin-right: 0;
			margin-bottom: 30px;
		}

		&__contentHolder {
			width: 100%;
		}


		&__header {
			font-size: 32px;
			margin-bottom: 15px;

		}

		// &__text {
		// 	font-size: 14px;
		// }
	}
}
</style>
