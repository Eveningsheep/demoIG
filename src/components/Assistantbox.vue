<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>
<template>
    <div class="bgimg">
      <h1 class="text">{{msg}}</h1>
    </div>
</template>
<style scoped>
  .bgimg {
    position: absolute;
    top: 0;
    left: 0;
    width: 25vw; /* 1/4 of the viewport width */
    height: auto; /* adjust the height automatically based on the width */
    background-image: url('../assets/assistantDialogBox.svg');
    background-size: cover; /* make sure the background image covers the whole div */
    background-repeat: no-repeat; /* prevent the background image from repeating */
  }
  .text{
    color: #fff;
    padding-top: 8.5vw;
    font-size:2.7em;
  }
</style>

  