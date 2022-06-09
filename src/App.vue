<script setup>
  import QuoteGenerator from './components/QuoteGenerator.vue'
  import TheAttribution from './components/TheAttribution.vue'
</script>


<template>
  <main>
    <QuoteGenerator />
  </main>
  <footer>
    <TheAttribution />
  </footer>
</template>


<style>
/* ==== VARIABLES ====*/
:root {
  --primary-color-1: hsl(193, 38%, 86%);
  --primary-color-2: hsl(150, 100%, 66%);

  --neutral-color-1: hsl(217, 19%, 38%);
  --neutral-color-2: hsl(217, 19%, 24%);
  --neutral-color-3: hsl(218, 23%, 16%);

  --font-size-quote: 28px;
  --font-weight: 800;
}

/* ==== FONTS ====*/
@font-face {
  font-family: Manrope-Extra-Light;
  src: url('./fonts/Manrope-Extra-Light.ttf');
}
@font-face {
  font-family: Manrope-Light;
  src: url('./fonts/Manrope-Light.ttf');
}
@font-face {
  font-family: Manrope-Medium;
  src: url('./fonts/Manrope-Medium.ttf');
}
@font-face {
  font-family: Manrope-Regular;
  src: url('./fonts/Manrope-Regular.ttf');
}
@font-face {
  font-family: Manrope-Semi-Bold;
  src: url('./fonts/Manrope-Semi-Bold.ttf');
}
@font-face {
  font-family: Manrope-Bold;
  src: url('./fonts/Manrope-Bold.ttf');
}
@font-face {
  font-family: Manrope-Extra-Bold;
  src: url('./fonts/Manrope-Extra-Bold.ttf');
}

/* ==== GENERAL STYLE ====*/
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0px;
  padding: 0px;
  font-weight: var(--font-weight);
}
html{
  height: 100%;
  background-color: var(--neutral-color-3);
}
body {
  position: relative;
  display:flex;
  flex-flow: column nowrap;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  color: white;
  background: black;
  transition: color 0.5s, background-color 0.5s;
  line-height: 1.6;
  font-family: Manrope-Medium, Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu,
    Cantarell, 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
  font-size: 15px;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#app{
  display:flex;
  flex-flow: column nowrap;
  justify-content: center;
  align-items: center;
  height: 100%;
}
main{
  display:flex;
  justify-content: center;
  align-items: center;
  flex-flow: column nowrap;
  background-color: var(--neutral-color-2);
  padding: 0px 25px;
  min-width: 340px ;
  width: 37.5%;
  border-radius: 10px;
}
h1{
  font-family: Manrope-Light ,Arial, Helvetica, sans-serif;
  font-weight: 100;
  font-size: 16px;
  color: var(--primary-color-2);
  margin: 35px 0px;
}
.advice__text{
  font-size:var(--font-size-quote);
  text-align: center;
  font-weight: 600;
  line-height: 1.7rem;
}
.stylish__container{
  display:flex;
  justify-content: space-between;
  align-items: center;
  flex-flow: row nowrap;
  height: 10px;
  width: 100%;
  padding: 30px 0px;
}
.stylish__bar{
  height: .5px;
  width: 100%;
  background: var(--primary-color-1);
}
.double__bar__container{
  min-width:50px;
  display:flex;
  justify-content: center;
  align-items: center;
  gap: 7px
}
.double__bar{
  width: 6px;
  height: 16px;
  background-color: white;
  border-radius: 3px;
}
.dice__circle{
  position: relative;
  top: 13px;
  display:flex;
  justify-content: center;
  align-items: center;
  background-color: var(--primary-color-2);
  padding: 20px;
  border-radius: 100%;
  margin: -20px;
  transition: .2s all;
  box-shadow: none;
}
.dice__circle:hover{ 
  box-shadow: 
  0px 0px 25px 0px hsl(178deg 77% 69%);
  }
footer{
  position: absolute;
  bottom: 10px;
}
.attribution { font-size: 11px; text-align: center; }
.attribution a { color: hsl(228, 45%, 44%); }
</style>
