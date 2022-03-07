<template>
  <div class="block">Click Here {{ delay }}</div>
</template>

<script>
export default {
  props: ["delay"],
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