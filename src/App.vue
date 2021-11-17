<template>
  <div id="app">
      <navigation-component></navigation-component>
      <contact-component></contact-component>
      <router-view></router-view>
      <footer-component></footer-component>
  </div>
</template>

<script>
import NavigationComponent from './components/NavigationComponent'
import ContactComponent from './components/ContactComponent'
import FooterComponent from './components/FooterComponent'

export default {
  components: {NavigationComponent, ContactComponent, FooterComponent}
}
</script>

<style lang="scss">

  #app
  {
    min-height: 100%;
    padding: 1.5rem;
    background-color: $color-secondary;
    user-select: none;
    position: relative;
  }

</style>
