<template>
  <div id="main">
    <div id="under">
      <button>足</button>
      <button>腿</button>
      <button>腹</button>
      
    </div>
    <inline-svg @click.native="clickHandler" :src="bodyImage" />
    <div id="upper">
      <button>头</button>
      <button>颈</button>
      <button>臂</button>
      <button>胸</button>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import InlineSvg from 'vue-inline-svg';
import bodyImage from '../assets/bodyImage.svg';

export default defineComponent({
  name: 'App',
  components: {
    'inline-svg': InlineSvg,
  },
  data() {
    return {
      bodyImage,
    };
  },
  methods: {
    clickHandler(event: MouseEvent) {
      console.log(event.target.id); // 这将打印出被点击元素的 id
    },
  },
});
</script>
<style scoped>
  #main {
    display: flex;
    position: relative;
  }
  #main button {
    padding: 1vw;
    background-color:  #9f2526;
    color: white;
    font-size: 2.5em;
    width: 12vw;
    margin: 2vw;
  }
  #under {
    display: flex;
    flex-direction: column-reverse;
    margin: 1vw;
    
  }
  #upper {
    display: flex;
    flex-direction: column;
    margin: 1vw;
  }
  inline-svg {
    position: relative;
    z-index: 1;
  }
</style>
