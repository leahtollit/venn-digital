<template>
  <Section class="textContent pos--rel">
		<div class="textContent__container container container--medium pos--rel flex flex--dir-c alignI--start">
			<div class="textContent__contentHolder pos--rel flex justifyC--start flex--dir-c">
				<h1 class="textContent__header fc--white fs--40">Join the crowd and become part of an award winning team</h1>
				<p class="textContent__text fc--white fs--24">Aliquam gravida odio at semper semper. In sagittis felis non pharetra dapibus. Maecenas</p>
			</div>
			<BaseBtn class="baseBtn--white">Careers</BaseBtn>
		</div>
  </section>
</template>

<script>
export default {
  name: 'TextContent',
}
</script>

<style lang="scss">
.textContent {
	background: red;
	padding: 107px 0;
	border-top: 1px solid $green;


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
