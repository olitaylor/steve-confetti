<template>
  <main>
    <button @click="start">Start</button>
    <button @click="stop">Stop</button>
  </main>
</template>

<script>
  import Vue from 'vue'
  import VueConfetti from 'vue-confetti'

  Vue.use(VueConfetti)

  export default {
    methods: {
      start() {
        this.$confetti.start({
          particles: [
            {
              type: 'image',
              size: 20,
              url: 'https://skypanel1.s3-eu-west-1.amazonaws.com/media_files/5cf6d33701062_Steve-Smiling.png',
            }
          ]
        });
      },
      stop() {
        this.$confetti.stop();
      },
    }
  }
</script>
