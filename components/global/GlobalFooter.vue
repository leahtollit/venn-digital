<template>
  <footer class="globalFooter pos--rel">
    <div class="globalFooter__container container flex">
    <!-- contact col -->
      <div class="globalFooter__contact flex flex--dir-c">
        <p class="globalFooter__heading fs--16 fc--white ff--inter">Contact Us</p>
        <div class="globalFooter__contactRow flex justifyC--between">
          <p class="globalFooter__subheading fs--14 fc--white ff--inter">Telephone</p>
          <a class="globalFooter__Contactlink fs--14 fc--white ff--inter" href="">+44 123 456 7890</a>
        </div>
        <div class="globalFooter__contactRow flex justifyC--between">
          <p class="globalFooter__subheading fs--14 fc--white ff--inter">Email</p>
          <a class="globalFooter__Contactlink fs--14 fc--white ff--inter" href="" target="_blank">enquires@domain.com</a>
        </div>
        <div class="globalFooter__connectRow flex flex--dir-c">
          <p class="globalFooter__heading fs--16 fc--white ff--inter">Connect with Us</p>
          <div class="globalFooter__socials flex alignI--center">
            <a
              href=""
              class="globalFooter__socialItem"
              target="_blank">
              <IconLinkedin class="globalFooter__icon globalFooter__icon--linkedin" />
            </a>
            <a
              href=""
              class="globalFooter__socialItem"
              target="_blank">
              <IconTwitter class="globalFooter__icon globalFooter__icon--twitter" />
            </a>
            <a
              href=""
              class="globalFooter__socialItem"
              target="_blank">
              <IconInstagram class="globalFooter__icon globalFooter__icon--instagram" />
            </a>
            <a
              href=""
              class="globalFooter__socialItem"
              target="_blank">
              <IconFacebook class="globalFooter__icon globalFooter__icon--facebook" />
            </a>
          </div>
        </div>
      </div>
      <!-- quick links -->
      <div class="globalFooter__navHolder flex">
        <div class="globalFooter__nav">
          <p class="globalFooter__heading fs--16 fc--white ff--inter">Quick Links</p>
          <div class="globalFooter__navLinks flex flex--dir-c">
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">Home
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">About Us
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">Clients
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">Candidates
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">Media Hub
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">Job Search
            </a>
          </div>
          <div class="globalFooter__nav">
          <p class="globalFooter__heading fs--16 fc--white ff--inter">Sectors</p>
          <div class="globalFooter__navLinks flex flex--dir-c">
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">Information Technology
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">Energy
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">Banking
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">Candidates
            </a>
            <a
              href=""
              class="globalFooter__navLink fs--11 fc--white ff--inter fw--500"
              target="_blank">Life Sciences
            </a>
            </div>
          </div>
        </div>
      </div>

      <!-- email col -->
      <div class="globalFooter__emailHolder">
        <p class="globalFooter__heading fs--16 fc--white ff--inter">Email Newsletter</p>
        <p class="globalFooter__text fs--11 fc--white ff--inter fw--500">Paragragh Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam gravida odio at semper semper. In </p>
        <div class="globalFooter__inputHolder flex">
          <input type="text" id="email" name="email" placeholder="Email Address" class="globalFooter__input fs--16 ff--inter fc--white">
          <button class="globalFooter__submitBtn">
          <IconEmail class="globalFooter__icon globalFooter__icon--email" />
          </button>
        </div>
      </div>
    </div>




    <div class="globalFooter__credits flex pos--rel justifyC--between alignI--center">
      <p class="globalFooter__copyright fs--12 ff--inter fw--500 fc--white">Copyright Venn</p>
      <div class="globalFooter__infoList flex">
        <a class="globalFooter__link" href="" target="_blank">
          <p class="globalFooter__linkText fs--12 ff--inter fw--500 fc--white">Privacy Policy</p>
        </a>
        <a class="globalFooter__link" href="" target="_blank">
          <p class="globalFooter__linkText fs--12 ff--inter fw--500 fc--white">Slavery &amp; Human Trafficking Statement</p>
        </a>
        <a class="globalFooter__link" href="" target="_blank">
          <p class="globalFooter__linkText fs--12 ff--inter fw--500 fc--white">Terms &amp; Conditions</p>
        </a>
      </div>
      <a class="globalFooter__link" href="" target="_blank">
        <p class="globalFooter__credit fs--12 ff--inter fw--500 fc--white">Site by Venn</p>
      </a>
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
    padding: 0 165px 93px;
    max-width: 1110px;
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
    max-width: 335px;
    width: 100%;
  }

  &__text {
    max-width: 255px;
    width: 100%;
    opacity: 0.5;
    margin-bottom: 21px;
  }
  
  &__contactRow {
  margin-bottom: 11px;

    &:nth-last-child(1){
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

    &--email {
      fill: $green;
      transition: fill 0.3s ease;
    }
  }

  &__credits {
    background: $greyDarker;
    padding: 21px 165px 22px;
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
    background: $green;
    max-width: 192px;
    border: 1px solid $white;
    padding: 14px 25px 15px;
  }
}
</style>
