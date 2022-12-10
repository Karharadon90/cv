<template>
  <div class="intro">
    <div class="intro__bg-left"></div>
    <div class="intro__bg-right"></div>
    <div class="intro__container">
      <div class="intro__content">
        <h2>Про себе</h2>
        <!-- <p>What I am all about</p> -->
      </div>
      <p class="intro__text">
        <pre> {{ intro.text }}</pre>
       
      </p>
    </div>
  </div>
</template>

<script>
import { intro } from "@/assets/contentText.js";
export default {
  data() {
    return {
      intro: intro,
    };
  },
};
</script>

<style land="scss" scoped>
.intro {
  display: flex;
  justify-content: center;
  position: relative;
}
.intro__container {
  width: 100%;
}

.intro__content {
  padding: 1.5rem;
  background: #fafafa;
  border-top: solid 1px rgb(237, 237, 237);
  border-bottom: solid 1px rgb(237, 237, 237);
}

.intro__content h2 {
  margin-bottom: 7px;
}
.intro__text {
  padding: 1.5rem;
}

@media screen and (min-width: 600px) {
  .intro__text {
    font-size: 17px;
  }
}

@media screen and (min-width: 760px) {
  .intro__content {
    padding: 2.75rem 3.05rem;
  }
  .intro__text {
    padding: 2.75rem 3.05rem;
  }
  @media screen and (min-width: 1024px) {
    .intro__bg-left {
      top: 0;
      left: 0;
      position: absolute;
      height: 100%;
      width: 50%;
      background: #f8f8f8;
    }
    .intro__bg-right {
      top: 0;
      right: 0;
      position: absolute;
      height: 100%;
      width: 50%;
      background: #fcfcfc;
    }
    .intro__container {
      display: flex;
      position: relative;
      z-index: 2;
      max-width: 1276px;
    }
    .intro__content {
      width: 30%;
      border: none;
      text-align: right;
      background: #f8f8f8;
    }
    .intro__text {
      width: 70%;
      background: #fcfcfc;
    }
  }
  @media screen and (min-width: 1200px) {
    .intro__content {
      padding: 4.6rem;
    }
    .intro__text {
      padding: 4.6rem;
    }
  }
}
</style>
