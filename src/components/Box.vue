<template>
  <div class="boxes">
    <div v-for="(box, index) in boxes" :key="index" class="box">
      <hgroup class="box__hg">
        <h3 class="box__heading">{{ box.heading }}</h3>
        <h4 class="box__subheading">{{ box.subheading }}</h4>
      </hgroup>
      <p class="box__employed">{{ box.employed }}</p>
      <div class="">

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Box',
  props: {
    boxes: {
      type: Array,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.box {
  margin: 0 0 3rem;
  padding: 2rem;
  background-color: var(--white);
  box-shadow: 0 0 20px rgba(0,0,0, 0.2);
  width: calc(100% - 20px);

  &__hg {
    font-family: var(--secondary-font);
  }

  &__heading {
    margin: 0;
    font-weight: 700;
    font-size: 1rem;
    text-transform: uppercase;
  }

  &__subheading {
    margin: 0 0 1rem;
    font-weight: 300;
    font-size: 0.8rem;

    @media screen and (min-width: 1280px) {
      font-size: 1rem;
    }
  }

  &__employed {
    margin: 0;
    font-size: 0.8rem;
    color: var(--medium-gray);
  }
}

</style>
