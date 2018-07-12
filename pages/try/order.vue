<template>
  <div>
    <div class="columns is-vcentered">
      <div class="column is-narrow">
        <div class="is-size-1">Order</div>
        <div class="is-size-5">Greater number come after each other.</div>
      </div>
      <div class="column is-narrow">
        <button class="button is-danger" @click="randomOrder()">Random new order</button>
      </div>
    </div>
    <div :style="{display: 'flex', backgroundColor: '#AAA'}">
      <Tile v-for="(order, index) in orders" :key="index" :style="{order: order}">{{index}} (order {{order}})</Tile>
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
      orders: [0,1,2,3,4,5,6,7,8,9]
    }
  },
  methods: {
    randomOrder () {
      const length = this.orders.length
      this.orders = []
      for (var i=0; i<length; i++) {
        this.orders.push(Math.floor(Math.random() * 10))
      }
    }
  }
}
</script>
