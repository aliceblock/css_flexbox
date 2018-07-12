<template>
  <div class="flex-tile" :style="tileStyle">
    <slot />
  </div>
</template>

<script>

function getRandomColor() {
  var letters = '0123456789ABCDE';
  var color = '#';
  for (var i = 0; i < 6; i++) {
    color += letters[Math.floor(Math.random() * letters.length)];
  }
  return color;
}

export default {
  data () {
    return {
      tileStyle: {
        backgroundColor: getRandomColor(),
        color: 'white',
        ...this.style
      }
    }
  }
}
</script>


<style lang="scss" scoped>
.flex-tile {
  display: flex;
  min-width: 100px;
  min-height: 100px;
  justify-content: center;
  align-items: center;
  margin: 5px;
}
</style>
