<template>
  <div class="header">
    <div class="header__bg"></div>

    <div class="cv__container">
      <div class="cv__content">
        <header>
          <div class="header__top">
            <div class="header__photo-wrap">
              <div class="header__photo">
                <img src="@/assets/HeaderPhoto.jpg" alt="my photo" />
              </div>
            </div>
            <div class="header__content-wrap">
              <div class="header__content">
                <div class="header__info">
                  <component-brand class="brand" />
                  <div class="header__subinfo" v-if="false">
                    <h2>Front-end Developer</h2>
                    <component-social-links />
                  </div>
                </div>
                <component-contacts :displayHr="true" />
              </div>
            </div>
          </div>
        </header>
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
};
</script>

<style lang="scss" scoped>
.cv__container {
  display: flex;
  justify-content: center;
}
.cv__content {
  width: 100%;
  padding: 1.5rem 1.5rem 0;
}

.header__top {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.header__photo {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 24.5px;
}

.header__photo img {
  display: block;
  width: 154px;
  height: 154px;
  border-radius: 50%;
}

.header__content-wrap {
  width: 100%;
}

.header__content {
  width: 100%;
}

.header__info {
  margin-bottom: 24.5px;
}

.firstname {
  display: block;
  font-weight: 300;
}
.lastname {
  display: block;
  color: #f8bb10;
  font-weight: 700;
  text-transform: uppercase;
}
.header__subinfo {
  font-size: 14px;
}
.header__subinfo h2 {
  text-align: center;
  font-weight: 300;
  font-size: 14px;
  padding: 20px 0;
}

.header__subinfo h2 {
  align-self: center;
}
.brand {
  text-align: center;
}

@media screen and (min-width: 600px) {
}

@media screen and (min-width: 760px) {
  .cv__content {
    padding: 3.05em 3.05em 1.1rem;
  }
  .header__photo img {
    width: 196px;
    height: auto;
  }
}

@media screen and (min-width: 1024px) {
  .header__bg {
    position: absolute;
    width: 50%;
    height: 100%;
    background: #fbfbfb;
    z-index: 1;
  }
  .cv__content {
    position: relative;
    max-width: 1276px;
    padding: 0;
    z-index: 2;
    background: white;
  }

  .header__top {
    width: 100%;
    flex-direction: row;
    justify-content: center;
  }
  .header__photo-wrap {
    width: 30%;
    height: 100vh;
    padding: 0 3.05rem;
    display: flex;
    justify-content: center;
    background-color: #fbfbfb;
  }
  .header__photo {
    flex: 0 0 auto;
  }

  .header__content-wrap {
    width: 70%;
    padding: 3.05rem 3.05rem 1.6rem;
    height: 100vh;
  }

  .header__content {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100%;
  }

  .header__subinfo h2 {
    text-align: left;
  }

  .contacts {
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
  }
  .header__subinfo {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
}
@media screen and (min-width: 1200px) {
  .header__photo img {
    width: 236px;
    height: auto;
  }
  .header__photo-wrap {
    padding: 0 4.6rem;
  }
  .header__content-wrap {
    padding: 3rem 4.6rem 1.6rem;
  }

  .header__subinfo h2 {
    font-size: 21px;
  }
  .brand {
    font-size: 67px;
  }
}
</style>
