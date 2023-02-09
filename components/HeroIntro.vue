<template>
  <Section class="heroIntro ">
		<div class="heroIntro__container container pos--rel flex flex--dir-c alignI--start">
			<div class="heroIntro__contentHolder pos--rel flex justifyC--start flex--dir-c">
				<h1 class="heroIntro__header fc--white fs--40">All the answers under one roof</h1>
				<p class="heroIntro__text fc--white fs--24">IT and Tech Recruitment for everything from start ups to large enterprises</p>
			</div>
			<BaseBtn class="baseBtn--green">Read More </BaseBtn>
		</div>
		<div class="heroIntro__nav flex flex--dir-c pos--abs y--center ">
			<div class="heroIntro__point"></div>
			<div class="heroIntro__point"></div>
			<div class="heroIntro__point"></div>
		</div>
  </section>
</template>

<script>
export default {
  name: 'HeroIntro',
}
</script>

<style lang="scss">
.heroIntro {
	width: 100%;
	height: 100vh;
	background: url('static/images/hero-image.jpg');
	background-repeat: no-repeat;
	background-size: cover;

	&__container {
		padding-top: 288px;
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
		right: 0;
	}
	&__point {
		width: 15px;
		height: 15px;
		background: $green;
		opacity: 0.3;
		border-radius: 50%;
		margin-bottom: 6px;
		transition: opacity .3s ease;

		&:nth-last-child(1) {
			margin-bottom: 0;
		}

		&:hover {
			cursor: pointer;
			opacity: 1;
		}
	}
	
}
</style>
