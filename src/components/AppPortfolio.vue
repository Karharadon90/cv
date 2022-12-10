<template>
  <div class="portfolio">
    <div class="portfolio__bg-left"></div>
    <div class="portfolio__bg-right"></div>
    <div class="portfolio__container">
      <div class="portfolio__title">
        <h2>portfolio</h2>
        <p>Here it gets interesting.</p>
      </div>
      <div class="portfolio__content">
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur
        modi explicabo labore ex optio iste, voluptas laborum tempore inventore?
        Voluptas recusandae molestias aspernatur asperiores fuga! Hic non velit
        accusantium? Voluptates.
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style land="scss" scoped>
.portfolio {
  display: flex;
  justify-content: center;
  position: relative;
}
.portfolio__container {
  width: 100%;
}

.portfolio__title {
  padding: 1.5rem;
  background: #fafafa;
  border-top: solid 1px rgb(237, 237, 237);
  border-bottom: solid 1px rgb(237, 237, 237);
}

.portfolio__title h2 {
  margin-bottom: 7px;
}
.portfolio__content {
  padding: 1.5rem 1.5rem 0;
}
.portfolio__timeline {
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
  .portfolio__title {
    padding: 2.75rem 3.05rem;
  }
  .portfolio__content {
    padding: 2.75rem 3.05rem 0;
  }
}

@media screen and (min-width: 1024px) {
  .portfolio__bg-left {
    top: 0;
    left: 0;
    position: absolute;
    height: 100%;
    width: 50%;
    background: #f8f8f8;
  }
  .portfolio__bg-right {
    top: 0;
    right: 0;
    position: absolute;
    height: 100%;
    width: 50%;
    background: #fcfcfc;
  }
  .portfolio__container {
    display: flex;
    position: relative;
    z-index: 2;
    max-width: 1276px;
  }
  .portfolio__title {
    width: 30%;
    border: none;
    text-align: right;
    background: #f8f8f8;
  }
  .portfolio__content {
    width: 70%;
    background: #fcfcfc;
  }
}
@media screen and (min-width: 1200px) {
  .portfolio__title {
    padding: 4.6rem;
  }
  .portfolio__content {
    padding: 3.75rem 4.6rem 0;
  }
}
</style>
