<template>
  <div class="me">
    <img class="me__photo" src="../assets/me2.jpg" alt="">
  </div>
</template>

<script>
export default {
  name: 'Me',
}
</script>

<style lang="scss" scoped>
.me {
  width: 100%;
  height: 100%;
  background-color: var(--white);
  grid-column: 2 / span 2;
  grid-row: 2;
  box-shadow: 0 0 50px rgba(0,0,0, 0.2);

  &__photo {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top center;
  }
}
</style>
