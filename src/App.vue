<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">

:root {
  --primary-font:     'Archivo Narrow', sans-serif;
  --secondary-font:   'Merriweather', serif;

  --darkest-gray:     #111;
  --dark-gray:        #333;
  --medium-gray:      #888;
  --light-gray:       #eee;

  --white:            #fff;
  --black:            #000;

  --desire:           rgb(230,57,70);
  --desire-dark:      rgb(189,47,58);
  --honeydew:         rgb(241,250,238);
  --baby-blue:        rgb(168,218,220);
  --queen-blue:       rgb(69,123,157);
  --space-cadet:      rgb(29,53,87);
  --space-cadet-dark: rgb(9,23,44);

  --container:        1280px;
  --scrollbar-width:  17px;
  --gutter:           20px;
  --header-height:    150px;
  --line-height:      1.5;
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
  background-color: var(--space-cadet);

  @media screen and (min-width: 1280px) {
    background-color: var(--honeydew);
  }
}
</style>
