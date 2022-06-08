<template>
  <div>
    <p class="text">Your Reaction time is = {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
  </div>
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
    if (this.score < 400) {
      console.log("component updated");
      this.rank = "Highly Reactive! keep going.";
    } else if (this.score < 600) {
      this.rank = "Good Reflexe! but you can do better.";
    } else {
      this.rank = "too Slow! wake up.";
    }
  },
};
</script>

<style>
.text {
  font-weight: 900;
  font-size: 1.3rem;
  color: rgb(131, 39, 39);
}
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
