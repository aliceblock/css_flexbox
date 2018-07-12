<template>
  <div>
    <div class="container">
      <div class="columns">
        <div class="column is-narrow">
          <nuxt-link class="button is-twitter" to="/try/flex-direction">
            Flex Direction
          </nuxt-link>
        </div>
        <div class="column is-narrow">
          <nuxt-link class="button is-twitter" to="/try/flex-wrap">
            Flex Wrap
          </nuxt-link>
        </div>
        <div class="column is-narrow">
          <nuxt-link class="button is-twitter" to="/try/justify-content">
            Justify Content
          </nuxt-link>
        </div>
        <div class="column is-narrow">
          <nuxt-link class="button is-twitter" to="/try/align-items">
            Align Items
          </nuxt-link>
        </div>
        <div class="column is-narrow">
          <nuxt-link class="button is-twitter" to="/try/align-content">
            Align Items
          </nuxt-link>
        </div>
        <div class="column is-narrow">
          <nuxt-link class="button is-primary" to="/try/order">
            Order
          </nuxt-link>
        </div>
        <div class="column is-narrow">
          <nuxt-link class="button is-primary" to="/try/flex-grow">
            Flex Grow
          </nuxt-link>
        </div>
        <div class="column is-narrow">
          <nuxt-link class="button is-primary" to="/try/flex-shrink">
            Flex Shrink
          </nuxt-link>
        </div>
        <div class="column is-narrow">
          <nuxt-link class="button is-primary" to="/try/flex-basis">
            Flex Basis
          </nuxt-link>
        </div>
        <div class="column is-narrow">
          <nuxt-link class="button is-primary" to="/try/align-self">
            Align Self
          </nuxt-link>
        </div>
      </div>
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
