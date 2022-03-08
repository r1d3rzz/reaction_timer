<template>
  <div class="block" v-if="showBlock">Click Here {{ delay }}</div>
</template>

<script>
export default {
  props: ["delay"],
  data() {
    return {
      showBlock: false,
    };
  },
  mounted() {
    setTimeout(() => {
      this.showBlock = true; //update
    }, this.delay);
  },
  updated() {
    console.log("update");
  },
  unmounted() {
    console.log("unmounted"); //is apperar when remove blockMdal from APP.uve
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