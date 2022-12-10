<template>
  <div class="footer">
    <div class="footer__bg-left"></div>
    <div class="footer__bg-right"></div>
    <div class="footer__container">
      <div class="footer__title">
        <h2>Contacts</h2>
        <p>Call me, maybe.</p>
      </div>
      <div class="footer__content">
        <component-contacts class="contacts" />
        <div class="footer__hr"></div>
        <div class="footer__info">
          <component-brand class="brand" />
          <component-social-links class="social__links" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ComponentBrand from "./ComponentBrand.vue";
import ComponentContacts from "./ComponentContacts.vue";
import ComponentSocialLinks from "./ComponentSocialLinks.vue";
export default {
  components: { ComponentContacts, ComponentSocialLinks, ComponentBrand },
  data() {
    return {};
  },
};
</script>

<style land="scss" scoped>
.footer {
  display: flex;
  position: relative;
  justify-content: center;
}
.footer__container {
  width: 100%;
}

.footer__title {
  padding: 1.5rem;
  background: #fbfbfb;
  border-top: solid 1px rgb(237, 237, 237);
  border-bottom: solid 1px rgb(237, 237, 237);
}

.footer__title h2 {
  margin-bottom: 7px;
}
.footer__content {
  padding: 1.5rem 1.5rem 0;
}
.footer__timeline {
  position: relative;
  border-left: 2px solid #ececec;
  margin-left: 12px;
}
.content__end {
  position: absolute;
  left: 5px;
  bottom: 0;
  width: 16px;
  height: 2px;
  background: #ececec;
}
.footer__hr {
  height: 2px;
  width: 100%;
  background: #ededed;
  margin-bottom: 3rem;
}
.footer__info {
  position: relative;
}
.contacts {
  text-align: left;
}

.social__links {
  justify-content: flex-start;
}

.brand {
  margin-bottom: 1rem;
}
@media screen and (min-width: 600px) {
  .footer__hr {
    margin-bottom: 5.5rem;
  }
  .social__links {
    position: absolute;
    right: 0;
    bottom: 0;
  }
}

@media screen and (min-width: 760px) {
  .footer__title {
    padding: 2.75rem 3.05rem;
  }
  .footer__content {
    padding: 2.75rem 3.05rem 0;
  }
}

@media screen and (min-width: 1024px) {
  .footer__bg-left {
    top: 0;
    left: 0;
    position: absolute;
    height: 100%;
    width: 50%;
    background: #fbfbfb;
  }
  .footer__bg-right {
    top: 0;
    right: 0;
    position: absolute;
    height: 100%;
    width: 50%;
    background: #fff;
  }
  .footer__container {
    display: flex;
    position: relative;
    z-index: 2;
    max-width: 1276px;
  }
  .footer__title {
    width: 30%;
    border: none;
    text-align: right;
    background: #fbfbfb;
  }
  .footer__content {
    width: 70%;
    background: #fff;
  }
}
@media screen and (min-width: 1200px) {
  .footer__title {
    padding: 4.6rem;
  }
  .footer__content {
    padding: 3.75rem 4.6rem 0;
  }
  .footer__hr {
    margin-bottom: 7.65rem;
  }
}
</style>
