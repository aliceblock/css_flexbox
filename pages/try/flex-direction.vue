<template>
  <div>
    <div class="columns is-vcentered">
      <div class="column is-narrow">
        <div class="is-size-1">Flex Direction</div>
        <div class="is-size-5">{{ 'Main axis: ' + (flexDirection == 'row'? 'Horizontal': 'Vertical') }}</div>
      </div>
      <div class="column">
        <button class="button is-danger" @click="flexDirection = 'row'">row</button>
        <button class="button is-danger" @click="flexDirection = 'row-reverse'">column-reverse</button>
        <button class="button is-danger" @click="flexDirection = 'column'">column</button>
        <button class="button is-danger" @click="flexDirection = 'column-reverse'">column-reverse</button>
      </div>
    </div>
    <div :style="{display: 'flex', backgroundColor: '#AAA', flexDirection: flexDirection}">
      <Tile style="max-width: 100px;">1</Tile>
      <Tile style="max-width: 100px;">2</Tile>
      <Tile style="max-width: 100px;">3</Tile>
      <Tile style="max-width: 100px;">4</Tile>
      <Tile style="max-width: 100px;">5</Tile>
      <Tile style="max-width: 100px;">6</Tile>
      <Tile style="max-width: 100px;">7</Tile>
      <Tile style="max-width: 100px;">8</Tile>
      <Tile style="max-width: 100px;">9</Tile>
      <Tile style="max-width: 100px;">10</Tile>
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
      flexDirection: 'row'
    }
  }
}
</script>