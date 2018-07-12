<template>
  <div>
    <div class="columns is-vcentered">
      <div class="column is-narrow">
        <span class="is-size-1">Align Items</span>
      </div>
      <div class="column is-narrow">
        <button class="button is-warning" @click="flexDirection = 'row'">row</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-warning" @click="flexDirection = 'column'">column</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignItems = 'flex-start'">flex-start</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignItems = 'flex-end'">flex-end</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignItems = 'center'">center</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignItems = 'baseline'">baseline</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignItems = 'stretch'">stretch</button>
      </div>
    </div>
    <div :style="{display: 'flex', backgroundColor: '#AAA', alignItems: alignItems, flexDirection: flexDirection, height: parentHeight}">
      <Tile>1</Tile>
      <Tile style="min-height: 150px; min-width: 150px;">2</Tile>
      <Tile>3</Tile>
      <Tile style="min-height: 200px; min-width: 200px;">4</Tile>
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
      alignItems: 'flex-start'
    }
  },
  computed: {
    parentHeight () {
      return this.flexDirection == 'row'? '500px': ''
    }
  }
}
</script>
