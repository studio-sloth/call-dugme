<template>
<div class="kollar" v-bind:style="{ 'background-image': 'url(' + img + ')' }">
  <button @mouseover=play @mouseleave=stop>
    call
  </button>
  <button @mouseover=play @mouseleave=stop>
    call
  </button>

  <audio hidden id="audio">
    <source src="./call-dugme.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>
</div>
</template>

<script>

export default {
  name: 'Dugme',
  data () {
    return {
      msg: 'iki kucuk call dugmesi',
      img: '',
      images: [
        'https://renk-magazin.de/wp-content/uploads/baris-manco_9180.jpg',
        'http://im.haberturk.com/2018/01/02/ver1514887806/1779642_4ab995fa5b6f599f7f1ee49bf23b67fe.jpg',
        'http://cdn.superhaber.tv/assets/uploads/images/content/2018/01/02/cropped_content_baris-manco-kimdir_t61NR445eS5m01s.jpg'
      ]
    }
  },
  methods: {
    play: function () {
      document.getElementById('audio').play()
      // this.changeBackground();
    },
    stop: function () {
      document.getElementById('audio').pause()
      // this.img = ''
    },
    changeBackground: function () {
      this.img = this.images[2]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
button {
  margin: 0 auto;
}
body {
  text-align: center;
}
.kollar {
  position: absolute;
  top: 50%;
  left: 50%;

}
</style>
