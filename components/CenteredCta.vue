<template>
  <Section class="centeredCta pos--rel">
		<div class="centeredCta__container pos--rel flex flex--dir-c alignI--center">
			<div class="centeredCta__contentHolder pos--rel flex justifyC--start flex--dir-c z--1">
				<h1 class="centeredCta__header fc--white fs--24 ta--center">Have a question? We want to hear from you! </h1>
				<p class="centeredCta__text fc--white fs--24 ta--center">Curabitur laoreet egestas!</p>
			</div>
				<BaseBtn class="baseBtn--white z--1">Get in Touch</BaseBtn>
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
	}

	&__header, &__text  {
		margin-bottom: 25px;
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
</style>
