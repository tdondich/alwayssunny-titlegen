<template>
  <div id="app">
    <p>"{{message}}"</p>
    <audio :src="'audio/' + this.audio + '.mp3'" autoplay="true"></audio>
  </div>
</template>

<script>
import VueAudio from 'vue-audio';

export default {
  name: 'app',
  components: {
    VueAudio
  },
  data: () => {
    return {
      message: 'Taylor breaks open source',
      audio: 'normal'
    }
  }
}
</script>

<style>
@font-face {
font-family: 'textile';
src: url('fonts/textile.woff2') format('woff2'),
      url('fonts/textile.woff') format('woff'),
      url('fonts/textile.ttf') format('truetype');
font-weight: normal;
font-style: normal;
}


body, html, #app {
  height: 100%;
  width: 100%;
  background-color: black;
}

#app {
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'textile', Helvetica, Arial, sans-serif;
  color: white;
  line-height: 1.5;
  font-size: 4em;
  text-align: center;
}
</style>
