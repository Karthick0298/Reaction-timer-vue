<template>
  <p>ReactionTime: {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
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
      this.rank = "Karthick fingers";
    } else if (this.score < 400) {
      this.rank = "Rapid reflexes";
    } else {
      this.rank = "snail pace...";
    }
  },
};
</script>

<style>
.rank {
  color: #0faf87;
  font-size: 26;
  font-weight: 500;
}
</style>