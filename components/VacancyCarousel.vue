<template>
  <Section class="vacancyCarousel pos--rel">
		<div class="vacancyCarousel__container container container--medium pos--rel flex flex--dir-c alignI--start">
      <div class="vacancyCarousel__headerHolder flex justifyC--between alignI--center">
				<h3 class="vacancyCarousel__header fs--40 fc--white fw--600 ff--montserrat lh--120">Latest Jobs</h3>
				<BaseBtn class="baseBtn baseBtn--green" link="/">Read More</BaseBtn>
			</div>
      <SliderJobs class="vacancyCarousel__carousel"/>
		</div>
  </section>
</template>

<script>
export default {
  name: 'VacancyCarousel',
}
</script>

<style lang="scss">
.vacancyCarousel {
  padding: 200px 0 306px;
  background: url('static/images/jellyfish.jpg');
	background-repeat: no-repeat;
	background-size: cover;
	background-position: center;


  &__headerHolder {
		width: 100%;
		margin-bottom: 37px;
	}
	
}

//----------------------------------------//
// 750
@include breakpoint(m) {
  .vacancyCarousel {
		padding: 100px 0 153px;

		&__headerHolder {
			flex-direction: column;
			align-items: flex-start;
		}

		&__headerHolder {
			margin-bottom: 18.5px;
		}

		&__header {
			margin-bottom: 25px;
		}
	}
}


//----------------------------------------//
// 600
@include breakpoint(s) {
  .vacancyCarousel {

		&__headerHolder {
			margin-bottom: 18.5px;
		}


		&__header {
			font-size: 32px;
		}


	}
}
</style>
