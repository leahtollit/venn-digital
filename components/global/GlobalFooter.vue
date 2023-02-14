<template>
  <footer class="globalFooter pos--rel">
    <div class="globalFooter__container container container--medium flex justifyC--between">
    <!-- contact col -->
      <div class="globalFooter__contact flex flex--dir-c">
        <p class="globalFooter__heading fs--16 fc--white ff--inter fw--900 lh--150">Contact Us</p>
        <div class="globalFooter__contactRow flex justifyC--between">
          <p class="globalFooter__subheading fs--14 fc--white ff--inter fw--500 lh--170" >Telephone</p>
          <a class="globalFooter__contactlink fs--14 fc--white ff--inter fw--900 lh--170" href="tel:01625788125">+44 123 456 7890</a>
        </div>
        <div class="globalFooter__contactRow flex justifyC--between">
          <p class="globalFooter__subheading fs--14 fc--white ff--inter fw--500 lh--170">Email</p>
          <a class="globalFooter__contactlink fs--14 fc--white ff--inter fw--900 lh--170" href="mailto:mailto:email@example.com" target="_blank">enquires@domain.com</a>
        </div>
        <div class="globalFooter__connectRow flex flex--dir-c">
          <p class="globalFooter__heading fs--16 fc--white ff--inter fw--900 lh--150">Connect with Us</p>
          <div class="globalFooter__socials flex alignI--center">
            <a
              href="https://www.linkedin.com/company/venn-digital"
              class="globalFooter__socialItem"
              target="_blank">
              <IconLinkedin class="globalFooter__icon globalFooter__icon--linkedin" />
            </a>
            <a
              href="https://twitter.com/venndigital"
              class="globalFooter__socialItem"
              target="_blank">
              <IconTwitter class="globalFooter__icon globalFooter__icon--twitter" />
            </a>
            <a
              href="https://www.instagram.com/lifeatvenn/"
              class="globalFooter__socialItem"
              target="_blank">
              <IconInstagram class="globalFooter__icon globalFooter__icon--instagram" />
            </a>
            <a
              href="https://www.facebook.com/venndigital"
              class="globalFooter__socialItem"
              target="_blank">
              <IconFacebook class="globalFooter__icon globalFooter__icon--facebook" />
            </a>
          </div>
        </div>
      </div>
      <!-- quick links -->
      <div class="globalFooter__navHolder flex">
        <div class="globalFooter__nav flex flex--dir-c">
          <p class="globalFooter__heading fs--16 fc--white ff--inter fw--900 lh--150">Quick Links</p>
          <div class="globalFooter__navLinks flex flex--dir-c">
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">Home
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">About Us
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">Clients
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">Candidates
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">Media Hub
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">Job Search
            </a>
          </div>
        </div>
          <div class="globalFooter__nav flex flex--dir-c">
          <p class="globalFooter__heading fs--16 fc--white ff--inter fw--900 lh--150">Sectors</p>
          <div class="globalFooter__navLinks flex flex--dir-c">
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">Information Technology
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">Energy
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">Banking
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">Candidates
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500 lh--170"
              target="_blank">Life Sciences
            </a>
          </div>
        </div>
      </div>

      <!-- email col -->
      <div class="globalFooter__emailHolder">
        <p class="globalFooter__heading fs--16 fc--white ff--inter fw--900 lh--150">Email Newsletter</p>
        <p class="globalFooter__text fs--11 fc--white ff--inter fw--400 lh--140">Paragragh Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In </p>
        <div class="globalFooter__inputHolder flex">
          <input type="text" id="email" name="email" placeholder="Email Address" class="globalFooter__input fs--16 ff--inter fc--white fw--700 lh--150">
          <button class="globalFooter__submitBtn">
          <IconEmail class="globalFooter__icon globalFooter__icon--email" />
          </button>
        </div>
      </div>
    </div>




    <div class="globalFooter__credits pos--rel">
      <div class="globalFooter__creditsHolder container container--medium pos--rel flex justifyC--between alignI--center">
      <p class="globalFooter__copyright fs--12 ff--inter fw--500 fc--white lh--200">Copyright Venn</p>
      <div class="globalFooter__infoList flex">
        <a class="globalFooter__link" href="" target="_blank">
          <p class="globalFooter__linkText fs--12 ff--inter fw--500 fc--white lh--200">Privacy Policy</p>
        </a>
        <a class="globalFooter__link" href="" target="_blank">
          <p class="globalFooter__linkText fs--12 ff--inter fw--500 fc--white lh--200">Slavery &amp; Human Trafficking Statement</p>
        </a>
        <a class="globalFooter__link" href="" target="_blank">
          <p class="globalFooter__linkText fs--12 ff--inter fw--500 fc--white lh--200">Terms &amp; Conditions</p>
        </a>
      </div>
      <a class="globalFooter__link" href="https://www.venndigital.co.uk/" target="_blank">
        <p class="globalFooter__credit fs--12 ff--inter fw--500 fc--white lh--200">Site by Venn</p>
      </a>
    </div>
    </div>
  </footer>
</template>

<script>
import IconFacebook from '~/assets/svgs/socials/facebook.svg?inline'
import IconTwitter from '~/assets/svgs/socials/twitter.svg?inline'
import IconLinkedin from '~/assets/svgs/socials/linkedin.svg?inline'
import IconInstagram from '~/assets/svgs/socials/instagram.svg?inline'
import IconEmail from '~/assets/svgs/socials/envelope-solid.svg?inline'


export default {
  name: 'GlobalFooter',
  components: {
    IconLinkedin,
    IconTwitter,
    IconFacebook, 
    IconInstagram,
    IconEmail
  }
}
</script>

<style lang="scss">
.globalFooter {
  padding: 69px 0 0;
  background: var(--greenDark);
  width: 100%;

  &__container {
    padding-bottom: 93px;
    // max-width: 1110px;
  }

  &__contactLink {
    position: relative;

      &::after {
      position: absolute;
      content: "";
      background: $white;
      width: 100%;
      height: 1px;
      bottom: -0.1875rem;
      left: 0;
      transform: scaleX(0);
      transition: transform .7s cubic-bezier(0.25, 0.1, 0.25, 1);
    }

    &:hover {
      &::after {
        transform: scaleX(1);
      }
    }
  }

  &__heading {
    margin-bottom: 21px;
  }

  &__contact {
    max-width: 281px;
    width: 100%;
  }

  &__connectRow {
    margin-top: 20px;
  }

  &__navHolder {
    flex-direction: row;
  }

  &__nav {
    &:nth-child(1) {
      margin-right: 98px;
    }
  }

  &__text {
    max-width: 255px;
    width: 100%;
    opacity: 0.5;
    margin-bottom: 21px;
  }
  
  &__contactRow {
    margin-bottom: 11px;

    &:nth-child(3) {
      margin-bottom: 0;
    }
  }
  

  &__socialItem {
    margin-right: 23px; 

    &:nth-last-child(1) {
      margin-right: 0;
    }
  }

  &__navLink {
    opacity: 0.5;
    margin-bottom: 11px;
    transition: opacity 0.3s ease;
    &:hover {
      opacity: 1;
    }
  }


  &__icon {
    fill: $white;
    transition: transform 0.3s ease;

    &--email {
      fill: $green;
      transition: fill 0.3s ease, transform 0.3s ease;
    }

    &:hover {
      transform: translateY(-2px);
    }
  }

  &__credits {
    background: $greyDarker;
    padding-top: 21px;
    padding-bottom: 22px;
    width: 100%;
  }

  &__copyright {
    opacity: 0.69;
  }

  &__link {
    margin-right: 10px;
    position: relative;
    opacity: 0.69;
    transition: opacity 0.3s ease;

    &:nth-last-child(1) {
      margin-right: 0;
    }

     &:hover {
      opacity: 1;
    }

  }

  &__copyright, &__credit, &__linkText {
    line-height: 24px;
  }

  &__inputHolder {
    max-width: 255px;
  }

  &__submitBtn {
    background: $white;
    border: none;
    padding: 18px;
    height: 50px;
    width: 63px;
    border: 1px solid $white;
    border-left-style: none;
    transition: background 0.3s ease;

    &:hover {
    background: $green;
    cursor: pointer;

      .globalFooter__icon--email {
        fill: $white;
      }
    }
  }

  &__input {
    border: none;
    background: $greenDark;
    max-width: 192px;
    height: 50px;
    border: 2px solid $white;
    padding: 14px 25px 15px;
    z-index: 1;

    &::placeholder {
      opacity: 1;
    }
  }
}


//----------------------------------------//
// 750
@include breakpoint(m) {
  .globalFooter { 

    &__container {
      flex-direction: column;
    }

    &__connectRow, &__navHolder {
      margin-bottom: 46px;
    }
  }
}
//----------------------------------------//
// 600
@include breakpoint(s) {
  .globalFooter {
    padding: 34px 0 0;


    &__container {
      padding-bottom: 93px;
    }

    &__credits {
      padding: 21px 24px 22px;
    }
  }
}

//----------------------------------------//
// 500
@include breakpoint(xs) {
  .globalFooter {
    &__nav {
      &:nth-child(1) {
        margin-right: 49px;
      }
    }

    &__connectRow, &__navHolder {
      margin-bottom: 25px;
    }

    &__text {
      max-width: 100%;
    }
  }
} 

//----------------------------------------//
// 400
@include breakpoint(xxs) {
  .globalFooter {
    &__nav {
      width: 100%;
      &:nth-child(1) {
        margin-right: 0;
        margin-bottom: 25px;
      }
    }
  }
} 
</style>
