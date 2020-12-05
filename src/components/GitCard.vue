<template>
  <article class="tip__card tip__card--git">
    <h2 class="tip__title">{{ title }}</h2>
    <h3 class="tip__subtitle">Cambiar el nombre de una rama en local y remoto</h3>
    <ul class="tip__list tip__list--columns">
      <li class="tip__item">
        <h4 class="tip__title tip__title--list">Renombra tu rama en local</h4>
        <ul class="tip__list">
          <li class="tip__item">
            <p class="tip__text tip__text--highlight">git branch -m <span>new-name</span></p>
            <p class="tip__text">Si estás en la rama</p>
          </li>
          <li class="tip__item">
            <p class="tip__text tip__text--highlight">git branch -m <span>old-name new-name</span></p>
            <p class="tip__text">Si estás en otra rama</p>
          </li>
        </ul>
      </li>
      <li class="tip__item">
        <h4 class="tip__title tip__title--list">Elimina la rama remota y pushea la nueva</h4>
        <p class="tip__text tip__text--highlight">git push origin :<span>old-name new-name</span></p>
      </li>
      <li class="tip__item">
        <h4 class="tip__title tip__title--list">Restablezca la rama con la nueva rama local</h4>
        <p class="tip__text tip__text--highlight">git push origin -u <span>new-name</span></p>
      </li>
    </ul>
  </article>
</template>

<script>
export default {
  name: 'GitCard',
  props: {
    title: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  // card general
  .tip__card {
    padding: 1.5rem;
    outline-width: 2px;
    outline-style: solid;
    outline-offset: -1rem;
    &--git {
      background-color:  #0C0C1E;
      outline-color: #1B2E3C;
    }
  }
  .tip__title {
    font-size: 2em;
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
    margin: 0.5rem 0;
    color:  #F3E3E2;
    &--list {
      font-weight: normal;
      font-size: 1em;
    }
  }
  .tip__subtitle {
    font-size: 1.5em;
    margin: 0.5rem 0;
    text-align: center;
    color: #F3E3E2;
  }
  .tip__text {
    color: #F3E3E2;
    font-size: 0.85em;

    &--highlight {
      color: #4D0011;
      background-color: #F3E3E2;
      padding: 8px;
      border-radius: 4px;
      font-weight: bold;
    }
  }
  // list
  .tip__list {
    display: grid;
    grid-template-columns: repeat( 2, minmax(100px, 1fr) );
    gap: 1.5rem;
    padding: 0.5rem;
    text-align: center;

    &--columns {
      grid-template-columns: minmax(0, 1fr);
    }
  }
  .tip__item {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;

    &> :not(last-child) {
      margin-bottom: 1rem;
    }
    &--opacity {
      position: relative;
    }
  }
</style>
