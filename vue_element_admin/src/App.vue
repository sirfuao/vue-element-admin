<template>
  <div id="app">
    <!-- 引入外部音乐 -->
    <audio id="audio" autoplay="autoplay" loop="loop">
      <source src="./assets/audios/music.mp3" type="audio/mpeg" />
    </audio>
    <!-- 路由占位符 -->
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
  mounted() {
    this.autoPlay()
  },
  methods: {
    autoPlay() {
      var bodyObj = document.getElementsByTagName('body')[0]
      var audio = document.getElementById('audio')
      console.log(bodyObj)
      bodyObj.onclick = function () {
        console.log('123')
        console.log(audio.paused)
         audio.play() // 播放

        // if (audio.paused) {
        //   // audio.paused  可以用来判断当前是否为暂停状态，true 就是暂停， false为播放状态
        //   audio.play() // 播放
        // } else {
        //   //  audio.pause();  暂停
        //   audio.play()
        // }
      }
    },
  },
}
</script>

<style>
</style>
