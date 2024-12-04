<script setup>
import { ref } from "vue";
const menuLinksText = ref([
  { id: 1, text: "About" },
  { id: 2, text: "Pricing" },
  { id: 3, text: "Company" },
  { id: 4, text: "Blog" },
]);
const socialLinks = ref([
  { className: "footer__social-link--facebook", id: 1, text: "Facebook." },
  { className: "footer__social-link--linkedin", id: 2, text: "LinkedIn." },
  { className: "footer__social-link--google", id: 3, text: "Google." },
]);
</script>

<template>
  <footer class="footer">
    <button class="footer__up">
      <span class="visually-hidden">К началу страницы.</span>
    </button>
    <div class="footer__content">
      <a class="footer__logo" href="#!">
        <img
          src="/images/footer-logo.svg"
          width="174"
          height="66"
          alt="Лого сайта."
        />
      </a>
      <ul class="footer__menu-list">
        <li
          class="footer__menu-item"
          v-for="item in menuLinksText"
          :key="item.id"
        >
          <a href="#!">{{ item.text }}</a>
        </li>
      </ul>
      <ul class="footer__social-list">
        <li
          class="footer__social-item"
          v-for="item in socialLinks"
          :key="item.id"
        >
          <a class="footer__social-link" :class="item.className" href="#!">
            <span class="visually-hidden">{{ item.text }}</span>
          </a>
        </li>
      </ul>
    </div>
    <p class="footer__copy">Copyright © 2019</p>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  position: relative;
  padding-top: 146px;
  background-color: $dark-color;

  @media (min-width: $desktop-width) {
    display: flex;
    padding: 39px 70px 31px;
  }
}

.footer__up {
  position: absolute;
  top: -41px;
  left: 135px;
  width: 104px;
  height: 104px;
  background: none;
  background-color: $default-red;
  background-image: url("../icons/arrow-up-footer.svg");
  background-repeat: no-repeat;
  background-position: 50%;
  border: none;
  border-radius: 50%;
  cursor: pointer;

  @media (min-width: $desktop-width) {
    top: -51px;
    right: 99px;
  }
}

.footer__logo {
  margin-bottom: 31px;

  @media (min-width: $desktop-width) {
    margin-right: 103px;
    margin-bottom: 0;
  }
}

.footer__content {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 35px;
  padding: 0 85px;

  @media (min-width: $desktop-width) {
    flex-direction: row;
    width: 100%;
    margin: 0;
    padding: 0;
  }
}

.footer__menu-list {
  margin: 0;
  margin-bottom: 35px;
  padding: 0;
  list-style: none;
  text-align: center;

  @media (min-width: $desktop-width) {
    display: flex;
    margin: 0;
  }
}

.footer__menu-item {
  margin-bottom: 36px;

  &:last-child {
    margin-bottom: 0;
  }

  @media (min-width: $desktop-width) {
    margin: 0;
    padding: 18px;
  }
}

.footer__menu-item a {
  font-weight: 700;
  font-size: 23px;
  line-height: 36px;
  text-decoration: none;
  color: $white-color;

  @media (min-width: $desktop-width) {
    font-size: 19px;
    line-height: 28px;
  }
}

.footer__social-list {
  display: flex;
  justify-content: space-between;
  width: 200px;
  margin: 0;
  padding: 0;
  list-style: none;

  @media (min-width: $desktop-width) {
    width: 121px;
    margin-right: 50px;
    margin-left: auto;
  }
}

.footer__social-link {
  display: block;
  width: 31px;
  height: 31px;

  &--facebook {
    background-image: url("../icons/facebook.svg");
  }

  &--linkedin {
    background-image: url("../icons/linkedin.svg");
  }

  &--google {
    background-image: url("../icons/google.svg");
  }
}

.footer__copy {
  margin: 0;
  padding-bottom: 35px;
  font-weight: 700;
  font-size: 24px;
  line-height: 37px;
  text-align: center;
  color: $white-color;

  @media (min-width: $desktop-width) {
    width: 278px;
    margin-top: 20px;
    padding: 0;
    font-size: 18px;
    line-height: 28px;
    text-align: left;
  }
}
</style>
