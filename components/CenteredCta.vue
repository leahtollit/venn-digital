<template>
  <Section class="centeredCta pos--rel">
		<div class="centeredCta__container container pos--rel flex flex--dir-c alignI--center">
			<div class="centeredCta__contentHolder pos--rel flex justifyC--start flex--dir-c z--1">
				<h4 class="centeredCta__header fc--white fs--24 ta--center ff--inter lh--150">Have a question? We want to hear from you! </h4>
				<p class="centeredCta__text fc--white fs--24 ta--center fw--300 ff--inter lh--150">Curabitur laoreet egestas!</p>
			</div>
				<BaseBtn class="baseBtn--white z--1" external :link="'mailto:mailto:email@example.com'">Get in Touch</BaseBtn>
		</div>
		<img class="centeredCta__bg pos--abs" src="/images/green-bg-shape.png" alt="">
  </section>
</template>

<script>
export default {
  name: 'CenteredCta',
}
</script>

<style lang="scss">
.centeredCta {
	background: $greenDark;
	padding: 61px 0 48px;
	margin: 117px auto 110px;
	max-width: 1110px;
	

	&__contentHolder {
		max-width: 555px;
		margin-bottom: 18px;
	}

	&__header, &__text  {
		width: 100%;
	}

	&__text {
		max-width: 543px;
	}

	&__bg {
		right: 0;
		top: 0;
		height: 100%;
		width: 100%;
		max-width: 783.67px;
	}
}

//----------------------------------------//
// 600
@include breakpoint(s) {
  .centeredCta {
		&__header, &__text  {
			margin-bottom: 15px;
		}

		&__header {
			font-size: 22px;
		}

		&__text {
			font-size: 18px;
		}
	}
}
</style>
