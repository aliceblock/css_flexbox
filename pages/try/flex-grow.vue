<template>
  <div>
    <div class="columns is-vcentered">
      <div class="column is-narrow">
        <span class="is-size-1">Flex Grow</span>
      </div>
      <div class="column">
        <button class="button is-danger" @click="randomOrder()">Random new grow</button>
      </div>
    </div>
    <div :style="{display: 'flex', backgroundColor: '#AAA'}">
      <Tile v-for="(grow, index) in growList" :key="index" :style="{flexGrow: grow}">{{index}} (flex-grow {{grow}})</Tile>
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
      growList: [1,2,3,4,5]
    }
  },
  methods: {
    randomOrder () {
      const length = this.growList.length
      this.growList = []
      for (var i=0; i<length; i++) {
        this.growList.push(Math.floor(Math.random() * length * 3))
      }
    }
  }
}
</script>