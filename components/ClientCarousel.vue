<template>
  <Section class="clientCarousel pos--rel">
		<div class="clientCarousel__container container container--medium pos--rel flex justifyC--center flex--dir-c ">
			<div class="clientCarousel__headerHolder pos--rel flex justifyC--center">
				<h1 class="clientCarousel__header fc--white ff--montserrat lh--120 fs--40 fw-600">A few of our fantastic clients</h1>
			</div>
			<SliderCarousel />
		</div>
  </section>
</template>

<script>
export default {
  name: 'ClientCarousel',
}
</script>

<style lang="scss">
.clientCarousel {
	// background: url('static/images/hero-image.jpg');
	background: $green;
	background-repeat: no-repeat;
	background-size: cover;
	padding: 111px 0 110px;

	&__headerHolder {
		margin-bottom: 53px;
		width: 100%;
	}
	
}

  //----------------------------------------//
// 600
@include breakpoint(s) {
  .clientCarousel {
		padding: 55px 0;


		&__header {
			font-size: 32px;
		}
	}
}
    
  
</style>
