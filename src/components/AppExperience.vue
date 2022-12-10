<template>
  <div class="experience">
    <div class="experience__bg-left"></div>
    <div class="experience__bg-right"></div>
    <div class="experience__container">
      <div class="experience__title">
        <h2>досвід</h2>
        <!-- <p>What I am all about</p> -->
      </div>
      <div class="experience__content">
        <div class="experience__timeline">
          <component-timeline
            :item="item"
            v-for="item in experience"
            :key="item"
          ></component-timeline>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { experience } from "@/assets/contentText.js";
import ComponentTimeline from "./ComponentTimeline.vue";

export default {
  components: { ComponentTimeline },
  data() {
    return {
      experience: experience,
    };
  },
};
</script>

<style land="scss" scoped>
.experience {
  display: flex;
  justify-content: center;
  position: relative;
}
.experience__container {
  width: 100%;
}

.experience__title {
  padding: 1.5rem;
  background: #fafafa;
  border-top: solid 1px rgb(237, 237, 237);
  border-bottom: solid 1px rgb(237, 237, 237);
}

.experience__title h2 {
  margin-bottom: 7px;
}
.experience__content {
  padding: 1.5rem 1.5rem 0;
}
.experience__timeline {
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

@media screen and (min-width: 760px) {
  .experience__title {
    padding: 2.75rem 3.05rem;
  }
  .experience__content {
    padding: 2.75rem 3.05rem 0;
  }
}

@media screen and (min-width: 1024px) {
  .experience__bg-left {
    top: 0;
    left: 0;
    position: absolute;
    height: 100%;
    width: 50%;
    background: #f8f8f8;
  }
  .experience__bg-right {
    top: 0;
    right: 0;
    position: absolute;
    height: 100%;
    width: 50%;
    background: #fcfcfc;
  }
  .experience__container {
    display: flex;
    position: relative;
    z-index: 2;
    max-width: 1276px;
  }
  .experience__title {
    width: 30%;
    border: none;
    text-align: right;
    background: #f8f8f8;
  }
  .experience__content {
    width: 70%;
    background: #fcfcfc;
  }
}
@media screen and (min-width: 1200px) {
  .experience__title {
    padding: 4.6rem;
  }
  .experience__content {
    padding: 3.75rem 4.6rem 0;
  }
}
</style>
