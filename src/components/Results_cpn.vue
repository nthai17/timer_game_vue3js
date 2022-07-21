<template>
  <div>
    <p>Reaction time: {{score}} ms</p>
    <p class="rank">{{rank}}</p>
  </div>
</template>

<script>
export default {
  props: [
    'score'
  ],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if (this.score < 250) this.rank = "World class"
    else if (this.score < 400) this.rank = "Medium"
    else this.rank = "Chicken boy"
  }
}
</script>

<style>
  .rank {
    font-size: 20px;
    font-weight: 700;
    color: #0faf87;
  }
</style>