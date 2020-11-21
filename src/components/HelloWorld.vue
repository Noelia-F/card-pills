<template>
  <article class="tip__card tip__card--animation">
    <h2 class="tip__title">{{ title }}</h2>
    <h3 class="tip__subtitle">Animaciones que no <span class="highlight">gastan</span> muchos recursos</h3>
    <ul class="tip__list">
      <li class="tip__item">
        <h4 class="tip__title tip__title--list">Position</h4>
        <div class="tip__example tip__example--position"></div>
        <p class="tip__text">transform: translate(50px, 0)</p>
      </li>
      <li class="tip__item">
        <h4 class="tip__title tip__title--list">Scale</h4>
        <div class="tip__example tip__example--scale"></div>
        <p class="tip__text">transform: scale(0.5)</p>
      </li>
      <li class="tip__item">
        <h4 class="tip__title tip__title--list">Rotation</h4>
        <div class="tip__example tip__example--rotation"></div>
        <p class="tip__text">transform: rotate(10deg)</p>
      </li>
      <li class="tip__item tip__item--opacity">
        <h4 class="tip__title tip__title--list">Opacity</h4>
        <div class="tip__dummy"></div>
        <div class="tip__example tip__example--opacity"></div>
        <p class="tip__text">opacity: 0.8</p>
      </li>
    </ul>
  </article>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    title: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  // card general
  .tip__card {
    padding: 1.5rem;
    outline-width: 2px;
    outline-style: solid;
    outline-offset: -1rem;
    &--animation {
      background-color: #F3E3E2;
      outline-color: #4D0011;
    }
  }
  .tip__title {
    font-size: 2em;
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
    margin: 0.5rem 0;
    &--list {
      font-weight: normal;
      font-size: 1em;
    }
  }
  .tip__subtitle {
    font-size: 1.5em;
    margin: 0.5rem 0;
    text-align: center;
  }
  .tip__text {
    color: #1B2E3C;
    font-size: 0.85em;
  }
  .highlight {
    font-weight: bold;
    color: #4D0011; 
  }
  // list
  .tip__list {
    display: grid;
    grid-template-columns: repeat( 2, minmax(100px, 1fr) );
    gap: 1.5rem;
    padding: 0.5rem;
    text-align: center;
  }
  .tip__item {
    display: flex;
    flex-direction: column;
    align-items: center;

    &> :not(last-child):not(.tip__dummy) {
      margin-bottom: 1rem;
    }
    &--opacity {
      position: relative;
    }
  }

  // example
  .tip__example {
    border-radius: 2px;
    height: 75px;
    width: 75px;
    background-color: #4D0011;
    animation-duration: 4s;
    animation-iteration-count: infinite;
    &--position {
      animation-name: position;
    }
    &--scale {
      animation-name: scale;
    }
    &--rotation {
      animation-name: rotation;
    }
    &--opacity {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      animation-name: opacity;
    }
  }
  .tip__dummy {
    border-radius: 50%;
    margin: 1rem 1rem 2rem 1rem;
    height: 43px;
    width: 43px;
    background-color: #0C0C1E;
  }

  // animations
  @keyframes position {
    from {transform: translate(0, 0)}
    to {transform: translate(50px, 0)}
  }
  @keyframes scale {
    from {transform: scale(1)}
    to {transform: scale(0.5)}
  }
  @keyframes rotation {
    from {transform: rotate(0)}
    to {transform: rotate(45deg)}
  }
  @keyframes opacity {
    from {opacity: 1}
    to {opacity: 0.4}
  }

</style>
