<template>
  <div>
    <div class="container">
      <nuxt-link class="button is-twitter" to="/try/flex-direction">
        Flex Direction
      </nuxt-link>
      <nuxt-link class="button is-twitter" to="/try/flex-wrap">
        Flex Wrap
      </nuxt-link>
      <nuxt-link class="button is-twitter" to="/try/justify-content">
        Justify Content
      </nuxt-link>
      <nuxt-link class="button is-twitter" to="/try/align-items">
        Align Items
      </nuxt-link>
      <nuxt-link class="button is-twitter" to="/try/align-content">
        Align Content
      </nuxt-link>
      <nuxt-link class="button is-primary" to="/try/order">
        Order
      </nuxt-link>
      <nuxt-link class="button is-primary" to="/try/flex-grow">
        Flex Grow
      </nuxt-link>
      <nuxt-link class="button is-primary" to="/try/flex-shrink">
        Flex Shrink
      </nuxt-link>
      <nuxt-link class="button is-primary" to="/try/flex-basis">
        Flex Basis
      </nuxt-link>
      <nuxt-link class="button is-primary" to="/try/align-self">
        Align Self
      </nuxt-link>
      <hr>
      <nuxt-child />
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Try ME'
  }
}
</script>

<style lang="scss" scoped>
div /deep/ .button {
  margin: 5px;
}
</style>
