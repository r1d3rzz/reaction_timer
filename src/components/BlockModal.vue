<template>
  <div class="block" v-if="showBlock" @click="stopTimer">
    Click Here {{ delay }}
  </div>
</template>

<script>
export default {
  props: ["delay"],
  data() {
    return {
      showBlock: false,
      score: 0,
      timer: null,
    };
  },
  mounted() {
    setTimeout(() => {
      this.showBlock = true; //update
      this.startTimer();
    }, this.delay);
  },
  methods: {
    startTimer() {
      this.timer = setInterval(() => {
        this.score += 50;
      }, 50);
    },
    stopTimer() {
      clearInterval(this.timer);
      console.log(this.score);
    },
  },
};
</script>

<style>
.block {
  width: 400px;
  height: 300px;
  background-color: aqua;
  margin: 30px auto;
  padding-top: 30px;
  border-radius: 5px;
}
</style>