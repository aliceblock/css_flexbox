<template>
  <div>
    <div class="columns is-vcentered">
      <div class="column is-narrow">
        <span class="is-size-1">Flex Basis</span>
      </div>
      <div class="column is-narrow">
        <input class="input" type="text" v-model="basis" placeholder="auto or 0 or % value">
      </div>
    </div>
    <div :style="{display: 'flex', backgroundColor: '#AAA'}">
      <Tile :style="{flexGrow: grow, flexBasis: basis}">11111111111111111111111111111111111111</Tile>
      <Tile :style="{flexGrow: grow, flexBasis: basis}">2222222222</Tile>
      <Tile :style="{flexGrow: grow, flexBasis: basis}">3</Tile>
      <Tile :style="{flexGrow: grow, flexBasis: basis}">4444</Tile>
    </div>
    <pre>
      {{showHTML}}
    </pre>
  </div>
</template>

<script>
import Tile from '~/components/Tile'
export default {
  components: {
    Tile
  },
  data () {
    return {
      basis: ''
    }
  },
  computed: {
    grow () {
      return this.basis == '0' || this.basis == 'auto' || this.basis == ''? 1: 0
    },
    showHTML () {
      return `
        <div :style="{display: 'flex', backgroundColor: '#AAA'}">
          <Tile :style="{flexGrow: ${this.grow}, flexBasis: ${this.basis || 'auto'}">11111111111111111111111111111111111111</Tile>
          <Tile :style="{flexGrow: ${this.grow}, flexBasis: ${this.basis || 'auto'}">2222222222</Tile>
          <Tile :style="{flexGrow: ${this.grow}, flexBasis: ${this.basis || 'auto'}">3</Tile>
          <Tile :style="{flexGrow: ${this.grow}, flexBasis: ${this.basis || 'auto'}">4444</Tile>
        </div>
      `
    }
  }
}
</script>
