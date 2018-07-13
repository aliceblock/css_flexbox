<template>
  <div>
    <div class="columns is-vcentered">
      <div class="column is-narrow">
        <span class="is-size-1">Justify Content</span>
      </div>
      <div class="column">
        <button class="button is-warning" @click="flexDirection = 'row'">row</button>
        <button class="button is-warning" @click="flexDirection = 'column'">column</button>
        <button class="button is-danger" @click="justifyContent = 'flex-start'">flex-start</button>
        <button class="button is-danger" @click="justifyContent = 'flex-end'">flex-end</button>
        <button class="button is-danger" @click="justifyContent = 'center'">center</button>
        <button class="button is-danger" @click="justifyContent = 'space-between'">space-between</button>
        <button class="button is-danger" @click="justifyContent = 'space-around'">space-around</button>
        <button class="button is-danger" @click="justifyContent = 'space-evenly'">space-evenly</button>
      </div>
    </div>
    <div :style="{display: 'flex', backgroundColor: '#AAA', justifyContent: justifyContent, flexDirection: flexDirection, height: parentHeight}">
      <Tile style="max-width: 100px;">1</Tile>
      <Tile style="max-width: 100px;">2</Tile>
      <Tile style="max-width: 100px;">3</Tile>
    </div>
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
      flexDirection: 'row',
      justifyContent: 'flex-start'
    }
  },
  computed: {
    parentHeight () {
      return this.flexDirection == 'row'? '': '500px'
    }
  }
}
</script>
