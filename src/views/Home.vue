<template>
  <div class="grid">

    <header class="site-header">
      <h1 class="site-header__heading">Martijn de Valk</h1>
      <h1 class="site-header__subheading">Creative Front-end Developer</h1>
    </header>

    <aside class="sidebar">
      <Contact />
    </aside>

    <Me />

    <Intro />

    <div class="bg">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1096 780.493">
        <g>
          <path fill="currentColor" d="M566.431 288.885l-7.794-7.794-10.392 10.392-10.392-10.392-7.794 7.794 10.392 10.391-10.392 10.392 7.794 7.794 10.392-10.392 10.392 10.392 7.794-7.794-10.392-10.392zM63.431 667.885l-7.794-7.794-10.392 10.391-10.392-10.391-7.794 7.794 10.392 10.391-10.392 10.392 7.794 7.794 10.392-10.392 10.392 10.392 7.794-7.794-10.392-10.392zM902.431 728.885l-7.794-7.794-10.392 10.391-10.392-10.391-7.794 7.794 10.392 10.391-10.392 10.392 7.794 7.794 10.392-10.392 10.392 10.392 7.794-7.794-10.392-10.392zM147.431 104.885l-7.794-7.794-10.392 10.391-10.392-10.391-7.794 7.794 10.392 10.391-10.392 10.392 7.794 7.794 10.392-10.392 10.392 10.392 7.794-7.794-10.392-10.392zM818.431 32.885l-7.794-7.794-10.392 10.392-10.392-10.392-7.794 7.794 10.392 10.391-10.392 10.392 7.794 7.794 10.392-10.392 10.392 10.392 7.794-7.794-10.392-10.392z"/>
          <path fill="none" stroke="currentColor" stroke-width="10" stroke-miterlimit="10" d="M199 705.993l19.999 18 19.995-18 19.997 18 19.998-18 20.001 18 20-18 20.001 18 20.001-18 20.004 18 20.004-18M603 178.993l19.999 18 19.995-18 19.997 18 19.998-18 20.001 18 20-18 20.001 18 20.001-18 20.004 18 20.004-18M766 561.993l19.999 18 19.995-18 19.997 18 19.998-18 20.001 18 20-18 20.001 18 20.001-18 20.004 18 20.004-18"/>
          <path fill="none" stroke="currentColor" stroke-width="7.42" stroke-miterlimit="10" d="M472.01 518.672l19.936-1.048 1.047-19.935 19.936-1.048 1.045-19.933 19.933-1.045 1.048-19.935 19.939-1.052 1.048-19.936 19.943-1.056 1.056-19.943M909.688 157.402l19.749 2.92 4.974-19.332 19.748 2.92 4.975-19.333 19.745 2.923 4.974-19.333 19.752 2.918 4.975-19.333 19.757 2.915 4.983-19.338"/>
          <path fill="none" stroke="currentColor" stroke-width="9.113" stroke-miterlimit="10" d="M260.938 126.782l-2.782-21.67-21.667-2.779-2.781-21.669-21.668-2.781-2.778-21.664-21.667-2.781-2.785-21.672-21.668-2.781-2.79-21.677-21.676-2.789"/>
          <circle fill="none" stroke="currentColor" stroke-width="7.42" stroke-miterlimit="10" cx="931.274" cy="501.767" r="18.274"/>
          <circle fill="currentColor" cx="682.049" cy="260.541" r="16.049"/>
          <circle fill="currentColor" cx="45.049" cy="43.541" r="16.049"/>
          <circle fill="currentColor" cx="463.049" cy="694.541" r="16.049"/>
          <circle fill="currentColor" cx="800.049" cy="444.541" r="16.049"/>
          <circle fill="none" stroke="currentColor" stroke-width="7.42" stroke-miterlimit="10" cx="165.274" cy="236.767" r="18.274"/>
          <circle fill="none" stroke="currentColor" stroke-width="7.42" stroke-miterlimit="10" cx="291.274" cy="609.767" r="18.274"/>
          <circle fill="none" stroke="currentColor" stroke-width="7.42" stroke-miterlimit="10" cx="884.274" cy="42.767" r="18.274"/>
          <path fill="none" stroke="currentColor" stroke-width="13.967" stroke-miterlimit="10" d="M184 443.656l187.163-187.163M184 513.493L371.163 326.33"/>
          <path fill="none" stroke="currentColor" stroke-width="10" stroke-miterlimit="10" d="M1008 348.493H818M972 384.493H782"/>
        </g>
      </svg>

    </div>

  </div>
</template>

<script>

import Contact from '@/components/Contact.vue'
import Me from '@/components/Me.vue'
import Intro from '@/components/Intro.vue'

export default {
  name: 'home',
  components: {
    Contact,
    Me,
    Intro
  }
}
</script>

<style lang="scss" scoped>
.grid {
  display: grid;
  grid-template-columns: minmax(200px, 300px) repeat(2, minmax(200px, 300px)) 100px minmax(500px, 600px) minmax(50px, 100px);
  grid-template-rows: 100px minmax(300px, calc(100vh - 200px)) 100px;
  height: 100vh;
}

.bg {
  grid-column: 3 / span 5;
  grid-row: 1 / span 3;
  z-index: -1;
  opacity: 0.1;
  svg {
    color: var(--desire);
    width: 100%;
    transform: scaleX(-1);
    object-fit: cover;
  }
}

.site-header {
  padding: 0 0 0 2rem;
  grid-column: 1 / span 2;
  grid-row: 1;
  z-index: 1;
  align-self: center;
  color: var(--white);
  font-family: var(--primary-font);

  &__heading {
    margin: 0 0 0.2rem;
    font-size: 1.8rem;
    line-height: 1;
    text-transform: uppercase;
    letter-spacing: -1px;
  }

  &__subheading {
    margin: 0;
    font-size: 0.75rem;
    line-height: 1;
    font-weight: 300;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
}

.sidebar {
  background: linear-gradient(to right, var(--desire) 0%, var(--desireDark) 100%);
  grid-column: 1 / span 2;
  grid-row: 1 / span 3;

  display: grid;
  grid-template-rows: 100px 1fr 100px;
}

</style>
