<template>
  <div class="timeline">
    <div class="point"></div>
    <div class="item__title">
      <p>{{ item.date }}</p>
      <h3>{{ item.company }}</h3>
      <h4>{{ item.profession }}</h4>
    </div>
    <div class="timeline__text">
      <p>
        <pre> {{ item.describe }}</pre>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["item"],
};
</script>

<style lang="scss" scoped>
.timeline {
  position: relative;
  padding: 0 0 0 1.5rem;
  padding-bottom: 2rem;
}

.point {
  position: absolute;
  top: 0;
  left: -6px;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: #f8bb10;
  box-shadow: 0 0 0 6px white;
}

.item__title p {
  opacity: 0.6;
  font-size: 10px;
  margin-bottom: 0.35rem;
}
.item__title h3 {
  color: #727272;
  text-transform: uppercase;
  font-size: 17px;
  line-height: 1.45;
  margin-bottom: 0.35rem;
}
.item__title h4 {
  font-size: 11px;
  font-weight: 500;
  margin-bottom: 0.35rem;
  color: #727272;
}

@media screen and (min-width: 760px) {
  .timeline {
    display: flex;
  }
  .item__title {
    width: 42%;
    margin-right: 49px;
  }
  .timeline__text {
    width: 58%;
  }
}
</style>
