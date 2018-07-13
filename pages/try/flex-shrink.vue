<template>
  <div>
    <div class="columns is-vcentered">
      <div class="column is-narrow">
        <div class="is-size-1">Flex Shrink</div>
        <div class="is-size-5">Greater number is smaller.</div>
      </div>
      <div class="column">
        <button class="button is-danger" @click="randomOrder()">Random new order</button>
        <button class="button is-danger" @click="setZero()">All zero</button>
      </div>
    </div>
    <div :style="{display: 'flex', backgroundColor: '#AAA'}">
      <Tile v-for="(shrink, index) in shrinkList" :key="index" :style="{flexShrink: shrink, width: '500px', minWidth: 'unset'}">{{index}} (shrink {{shrink}})</Tile>
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
      shrinkList: [1,2,3]
    }
  },
  methods: {
    randomOrder () {
      const length = this.shrinkList.length
      this.shrinkList = []
      for (var i=0; i<length; i++) {
        this.shrinkList.push(Math.floor(Math.random() * length))
      }
    },
    setZero () {
      const length = this.shrinkList.length
      this.shrinkList = []
      for (var i=0; i<length; i++) {
        this.shrinkList.push(0)
      }
    }
  }
}
</script>