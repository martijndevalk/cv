<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">

:root {
  --primary-font:   'Archivo Narrow', sans-serif;
  --secondary-font: 'Merriweather', serif;

  --darkest-gray:   #111;
  --dark-gray:      #333;
  --medium-gray:    #888;
  --light-gray:     #eee;

  --white:          #fff;
  --black:          #000;

  --desire:      rgba(230, 57,  70,  1);
  --desireDark:  rgba(189, 47, 58, 1);
  --honeydew:    rgba(241, 250, 238, 1);
  --baby-blue:   rgba(168, 218, 220, 1);
  --queen-blue:  rgba(69,  123, 157, 1);
  --space-cadet: rgba(29,  53,  87, 1);

  --container:       1280px;
  --scrollbar-width: 17px;
  --gutter:          20px;
  --header-height:   150px;
  --line-height:     1.5;
}

html, body, #app {
  height: 100%;
}

html {
  width: 100vw;
  overflow-x: hidden;
  overflow-y: auto;
  box-sizing: border-box;
}

*, *::before, *::after {
  box-sizing: inherit;
}

body {
  margin: 0;
  font-family: var(--secondary-font);
  color: var(--dark-gray);
  background-color: var(--honeydew);
}

#app {

}
</style>
