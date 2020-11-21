<template>
  <div class="tips__wrapper">
    <HelloWorld title="Animaciones"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
  @import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

  // css reset
  html, body, div, span, applet, object, iframe, table, caption,
  tbody, tfoot, thead, tr, th, td, del, dfn, em, font, img, ins,
  kbd, q, s, samp, small, strike, strong, sub, sup, tt, var,
  h1, h2, h3, h4, h5, h6, p, blockquote, pre, a, abbr,
  acronym, address, big, cite, code, dl, dt, dd, ol, ul, li,
  fieldset, form, label, legend {
      vertical-align: baseline;
      font-family: inherit;
      font-weight: inherit;
      font-style: inherit;
      font-size: 100%;
      outline: 0;
      padding: 0;
      margin: 0;
      border: 0;
  }
  :focus {
      outline: 0;
  }
  body {
      background: white;
      line-height: 1;
      color: black;
  }
  ol, ul {
      list-style: none;
  }
  table {
      border-collapse: separate;
      border-spacing: 0;
  }
  caption, th, td {
      font-weight: normal;
      text-align: left;
  }
  blockquote:before, blockquote:after, q:before, q:after {
      content: "";
  }
  blockquote, q {
      quotes: "" "";
  }

  // apply font
  * {
    box-sizing: border-box;
    font-family: 'roboto';
    font-size: 16px;
    color: #0C0C1E;
  }

  // styles
  .tips__wrapper {
    display: grid;
    grid-template-columns: repeat( auto-fit, minmax(250px, 1fr) );
  }
</style>
