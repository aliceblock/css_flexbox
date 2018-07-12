<template>
  <div>
    <div class="columns is-vcentered">
      <div class="column is-narrow">
        <span class="is-size-1">Align Content</span>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignContent = 'flex-start'">flex-start</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignContent = 'flex-end'">flex-end</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignContent = 'center'">center</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignContent = 'space-between'">space-between</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignContent = 'space-around'">space-around</button>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="alignContent = 'stretch'">stretch</button>
      </div>
    </div>
    <div :style="{display: 'flex', backgroundColor: '#AAA', height: '300px', flexWrap: 'wrap', alignContent: alignContent}">
      <div style="display: flex;">
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
      </div>
      <div style="display: flex;">
        <Tile>11</Tile>
        <Tile>12</Tile>
        <Tile>13</Tile>
        <Tile>14</Tile>
        <Tile>15</Tile>
        <Tile>16</Tile>
        <Tile>17</Tile>
        <Tile>18</Tile>
        <Tile>19</Tile>
        <Tile>10</Tile>
      </div>
    </div>
    <div :style="{display: 'flex', marginTop: '10px', backgroundColor: '#AAA', height: '300px', flexWrap: 'wrap', alignContent: alignContent}">
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
      <Tile>10</Tile>
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
      alignContent: 'flex-start'
    }
  }
}
</script>
