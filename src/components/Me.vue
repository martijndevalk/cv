<template>
  <div class="me">
    <img class="me__photo" src="https://res.cloudinary.com/plat-vlak/image/upload/q_auto,f_auto/e_grayscale/e_tint:100:09172c:0p:3864a3:100p/v1539778843/martijn.jpg" alt="">
  </div>
</template>

<script>
export default {
  name: 'Me',
}
</script>

<style lang="scss" scoped>
.me {
  grid-column: 1;
  grid-row: 2;
  width: 100%;
  height: 100vh;
  background: url('https://res.cloudinary.com/plat-vlak/image/upload/q_auto,f_auto/e_grayscale/e_tint:100:09172c:0p:3864a3:100p/v1539786805/martijn2.jpg') top center / cover no-repeat;
  box-shadow: 0 0 50px rgba(0,0,0, 0.2);
  position: sticky;
  top: 0;

  @media screen and (max-width: 1279px) {
    opacity: 0.5;
  }

  @media screen and (min-width: 1280px) {
    grid-column: 2 / span 2;
    grid-row: 2;
    height: 100%;
  }

  &:hover,
  &:focus {
    .me__photo {
      opacity: 0;
    }
  }

  &__photo {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top center;
    transition: opacity 300ms linear;
  }
}
</style>
