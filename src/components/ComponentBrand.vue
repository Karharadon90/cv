<template>
  <div class="brand">
    <h1>
      <span class="firstname">Андрій</span>
      <span class="lastname">Волошин</span>
    </h1>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.brand {
  font-size: 44px;
}

.brand h1 {
  font-size: 1em;
  line-height: 0.91;
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
@media screen and (min-width: 1024px) {
  .brand h1 {
    text-align: left;
  }
}


</style>
