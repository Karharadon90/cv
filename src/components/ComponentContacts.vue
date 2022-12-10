<template>
  <div class="contacts">
    <div v-if="displayHr" class="header__hr"></div>
    <div class="contacts__content">
      <div class="contact__item">
        <h4>Місто</h4>
        <address>Україна, м.Харків</address>
      </div>
      <div class="contact__item">
        <h4>Телефон</h4>
        <p>+38(099)111-51-91</p>
      </div>
      <!-- <div class="contact__item">
        <a href="#" class="contact__link">
          <h4>Web</h4>
          <p>youtube.com</p>
        </a>
      </div> -->
      <div class="contact__item">
        <h4>Почта</h4>
        <p>VoloshinAndy@gmail.com</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["displayHr"],
};
</script>

<style lang="scss" scoped>
.contacts {
  text-align: center;
}
.header__hr {
  width: 100%;
  height: 2px;
  background-color: rgb(237, 237, 237);
  margin-bottom: 24.5px;
}
.contacts__content {
  display: flex;
  flex-direction: column;
}
.contact__item {
  margin-bottom: 24.5px;
}
.contact__item h4 {
  color: #727272;
  font-weight: 600;
  margin-bottom: 8px;
}
.contact__item address {
  font-weight: 400;
  font-style: normal;
}

.contact__link {
  transition: color 0.15s linear;
  &:hover {
    color: #f8bb10;
  }
}

.text__align-start {
  align-items: flex-start;
}

@media screen and (min-width: 600px) {
  .contacts__content {
    width: 100%;
    flex-direction: row;
    flex-wrap: wrap;
  }

  .contact__item {
    width: 50%;
  }
}
@media screen and (min-width: 760px) {
  .header__photo img {
    width: 196px;
    height: 196px;
  }
  .contact__item {
    width: 25%;
    width: 33%;
    align-items: flex-start;
    text-align: left;
  }
  .contact__link {
    align-items: flex-start;
  }
}
</style>
