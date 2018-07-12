<template>
  <div>
    <div class="columns is-vcentered">
      <div class="column is-narrow">
        <span class="is-size-1">Flex Wrap</span>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="flexWrap = 'nowrap'">nowrap</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="flexWrap = 'wrap'">wrap</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="flexWrap = 'wrap-reverse'">wrap-reverse</button>
      </div>
    </div>
    <div :style="{display: 'flex', backgroundColor: '#AAA', flexWrap: flexWrap}">
      <Tile>1</Tile>
      <Tile>2</Tile>
      <Tile>3</Tile>
      <Tile>4</Tile>
      <Tile>5</Tile>
      <Tile>6</Tile>
      <Tile>7</Tile>
      <Tile>8</Tile>
      <Tile>9</Tile>
      <Tile>10</Tile>
      <Tile>11</Tile>
      <Tile>12</Tile>
      <Tile>13</Tile>
      <Tile>14</Tile>
      <Tile>15</Tile>
      <Tile>16</Tile>
      <Tile>17</Tile>
      <Tile>18</Tile>
      <Tile>19</Tile>
      <Tile>20</Tile>
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
      flexWrap: 'nowrap'
    }
  }
}
</script>

<style lang="scss" scoped>
.flex-tile {
  width: 100px;
  min-width: unset !important;
}
</style>
