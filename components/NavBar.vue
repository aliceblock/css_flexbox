<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item" href="https://bulma.io">
        <img src="https://bulma.io/images/bulma-logo.png" alt="Bulma: a modern CSS framework based on Flexbox" width="112" height="28">
      </a>

      <a role="button" class="navbar-burger" :class="{'is-active': menuActive}" aria-label="menu" aria-expanded="false" @click="menuActive = !menuActive">
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>
    <div class="navbar-menu" :class="{'is-active': menuActive}">
      <div class="navbar-start">
        <nuxt-link class="navbar-item" active-class="is-active" to="/" exact>
          Home
        </nuxt-link>
        <nuxt-link class="navbar-item" active-class="is-active" to="/try">
          Try Flex
        </nuxt-link>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      menuActive: false
    }
  }
}
</script>
