
<template>
  <Section class="statText pos--rel">
		<div class="statText__container container container--medium flex justifyC--between">
			<div class="statText__contentHolder flex z--1">
				<h2 class="statText__header fs--40 fw--600 fc--white ff--montserrat lh--125">Who are Venn Digital</h2>
				<p class="statText__text fc--white fs--24 fw--400 ff--montserrat lh--150">Large Paragragh Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In sagittis felis non pharetra dapibus. Maecenas in laoreet justo, at maximus nibh. Curabitur laoreet egestas dui vitae aliquet.</p>
				<BaseBtn class="baseBtn baseBtn--white">Read More</BaseBtn>
			</div>
			<div class="statText__holder z--1">
        <div class="statText__items">
          <div v-for="(el, i) in items" :key="el + i" class="statText__itemHolder">
            <div class="statText__body flex alignI--center justifyC--center">

              <div class="statText__copyHolder flex flex--dir-c">
                <p class="statText__statistic fw--700 fs--60 fc--white pos--rel lh--120 ff--montserrat">{{ el.statistic }}</p>
                <p class="statText__title fs--12 lh--125 fw--700 fc--white ff--montserrat pos--rel">
                  {{ el.text }}
                </p>
              </div>
            </div>
					</div>
				</div>
			</div>
		</div>
		<!-- <img class="statText__bg pos--abs" src="/images/green-bg-shape-larger.png" alt=""> -->

  </section>
</template>

<script>
export default {
  name: 'StatText',
	data() {
		return {
			items: [
				{
        	statistic: '1,790',
        	text: 'Live Jobs'
        },
				{
        	statistic: '1,790',
        	text: 'Live Jobs'
        },
				{
        	statistic: '1,790',
        	text: 'Live Jobs'
        },
				{
        	statistic: '1,790',
        	text: 'Live Jobs'
        },
			]
		}
	}
}
</script>

<style lang="scss">
.statText {
	background: url('static/images/statistic-bg.jpg');
	background-repeat: no-repeat;
	background-size: cover;
	padding-top: 117px;
	padding-bottom: 203px;

	&__header {
		max-width: 254px;
		margin-bottom: 28px;
		line-height: 49px;
	}

	&__contentHolder {
		max-width: 540px;
		width: 50%;
	}

	&__text {
		width: 100%;
		margin-bottom: 31px;
		line-height: 36px;
	}

	&__holder {
    width: calc(50% - 95px);
		margin-left: 95px;
    max-width: 475px;
  }

  &__body {
    flex-direction: row;
    position: relative;
    top: 50%;
    width: 220px;
    height: 100%;
  }

	&__title {
		text-align: center;
	}

	&__statistic {
		margin-bottom: 5px;
	}

  &__itemHolder {
    position: relative;
    display: flex;
    width: 100%;
    margin-bottom: 0;

    &:nth-last-of-type(1) {
      margin-bottom: 0;
    }

    // &:nth-child(1) {
    //   transition-delay: 0.3s;
    // }

    // &:nth-child(2) {
    //   transition-delay: 0.6s;
    // }

    // &:nth-child(3) {
    //   transition-delay: 0.9s;
    // }

    // &:nth-child(4) {
    //   transition-delay: 1.2s;
    // }

    // &:nth-child(5) {
    //   transition-delay: 1.5s;
    // }

    &:nth-child(odd) {
      justify-content: flex-end;
      transform: translateX(35px);
    }

    // transform: translateX(-30px);
    // opacity: 0;
    // transition: transform 0.5s, opacity 0.5s;
  }

	&__bg {
		right: 0;
		top: 0;
		z-index: 0;
		max-width: 990.34px;
	}


}

//----------------------------------------//
// 600
@include breakpoint(s) {
  .statText {
		padding-top: 58px;
		padding-bottom: 100px;


		&__header {
			font-size: 32px;
		}

		&__text {
			font-size: 18px;
		}

		&__container {
			flex-direction: column;
		}

		&__contentHolder {
			margin-bottom: 28px;
		}

		&__contentHolder, &__holder {
			width: 100%;
		}

		&__holder {
			margin-left: 0;
		}

		&__contentHolder, &__header, &__text {
			max-width: 100%;
		}

		&__body {
      margin-bottom: 32px;
      width: 100%;
      max-width: 100%;
      height: 100%;
      margin-right: 0;
      flex-direction: column;
      align-items: center;
      justify-content: center;

      &:nth-last-of-type(0) {
        margin-bottom: 0;
      }
    }

    &__itemHolder {
      margin-bottom: 0;

			&:nth-child(odd) {
      	transform: translateX(0);
			}
    }
	
	}
}
</style>
