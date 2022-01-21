<template>
  <p>Reaction time = {{ score }} ms</p>
  <p clas="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "Ninja Fingers";
    } else if (this.score < 400) {
      this.rank = "Rapid Refexes";
    } else {
      this.rank = "Snail pace...";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4rem;
  color: crimson;
  font-weight: bold;
}
</style>