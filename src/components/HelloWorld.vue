<template>
  <article>
    <h2>{{ title }}</h2>
    <h3>Animaciones que no <span>gastan</span> muchos recursos</h3>
    <ul>
      <li>
        <h4>Position</h4>
        <p>transform: translate(10px, 10px)</p>
      </li>
      <li>
        <h4>Scale</h4>
        <p>transform: scale(0.5)</p>
      </li>
      <li>
        <h4>Rotation</h4>
        <p>transform: rotate(10deg)</p>
      </li>
      <li>
        <h4>Opacity</h4>
        <p>opacity: 0.8</p>
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
<style scoped lang="scss">
</style>
