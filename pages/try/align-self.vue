<template>
  <div>
    <div class="columns is-vcentered">
      <div class="column is-narrow">
        <span class="is-size-1">Align Self</span>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignSelf = 'auto'">auto</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignSelf = 'flex-start'">flex-start</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignSelf = 'flex-end'">flex-end</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignSelf = 'center'">center</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignSelf = 'baseline'">baseline</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignSelf = 'stretch'">stretch</button>
      </div>
    </div>
    <div :style="{display: 'flex', backgroundColor: '#AAA', height: '400px', alignItems: 'center'}">
      <Tile>1</Tile>
      <Tile style="min-height: 150px" :style="{alignSelf: alignSelf == 'baseline'? 'baseline': 'auto'}">2</Tile>
      <Tile :style="{alignSelf: alignSelf}">3</Tile>
      <Tile style="min-height: 200px">4</Tile>
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
      alignSelf: 'auto'
    }
  }
}
</script>
