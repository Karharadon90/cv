<template>
  <div class="social__links">
    <ul class="social__list">
      <li class="social__item">
        <a
          href="https://github.com/AndrewVoloshin"
          class="header__link"
          target="blank"
        >
          <font-awesome-icon icon="fa-brands fa-github" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.social__links {
  display: flex;
  justify-content: center;
}

.fa-github {
  font-size: 25px;
  color: #c6c6c6;
  border: 2px solid #f8bb10;
  padding: 2px;
  background-color: rgb(237, 237, 237);
  border-radius: 3px;
  border: 2px solid rgb(237, 237, 237);
  text-align: center;
  transition: all 0.15s linear;
}

.fa-github:hover {
  color: #f8bb10;
  border: 2px solid rgb(237, 237, 237);
  background: white;
}
.header__link {
  display: block;
  width: 33px;
  height: 33px;
}

@media screen and (min-width: 1200px) {
  .fa-github {
    font-size: 31px;
  }
}
</style>
