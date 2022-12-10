<template>
  <div class="skills">
    <div class="skills__bg-left"></div>
    <div class="skills__bg-right"></div>
    <div class="skills__container">
      <div class="skills__content">
        <h2>релевантний досвід</h2>
        <!-- <p>What I am all about</p> -->
      </div>
      <p class="skills__text">
        <!-- Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima omnis -->
        <pre> {{ relevantExperience.text }}</pre>
       <!-- {{ relevantExperience.text }} -->
      </p>
    </div>
  </div>
</template>

<script>
import {relevantExperience} from "@/assets/contentText.js";
export default {
  data() {
    return {
      relevantExperience: relevantExperience,
    };
  },
};
</script>

<style land="scss" scoped>
.skills {
  display: flex;
  justify-content: center;
  position: relative;
}
.skills__container {
  width: 100%;
}

.skills__content {
  padding: 1.5rem;
  background: #fafafa;
  border-top: solid 1px rgb(237, 237, 237);
  border-bottom: solid 1px rgb(237, 237, 237);
}

.skills__content h2 {
  margin-bottom: 7px;
}
.skills__text {
  padding: 1.5rem 1.5rem 0;
}
 

@media screen and (min-width: 600px) {
  .skills__text {
    font-size: 17px;
  }


}

@media screen and (min-width: 760px) {
  .skills__content {
    padding: 2.75rem 3.05rem;
  }
  .skills__text {
    padding: 2.75rem 3.05rem 0;
  }
  @media screen and (min-width: 1024px) {
    .skills__bg-left {
      top: 0;
      left: 0;
      position: absolute;
      height: 100%;
      width: 50%;
      background: #fbfbfb;
    }
    .skills__bg-right {
      top: 0;
      right: 0;
      position: absolute;
      height: 100%;
      width: 50%;
      background: #fff;
    }
    .skills__container {
      display: flex;
      position: relative;
      z-index: 2;
      max-width: 1276px;
    }
    .skills__content {
      width: 30%;
      border: none;
      text-align: right;
      background: #fbfbfb;
    }
    .skills__text {
      width: 70%;
      background: #fff;
    }
  }
  @media screen and (min-width: 1200px) {
    .skills__content {
      padding: 4.6rem;
    }
    .skills__text {
      padding: 4.6rem;
    }
  }
}
</style>
