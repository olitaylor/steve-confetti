<template>
  <main>
    <button @click="startSteve">Start stevefetti</button>
    <button @click="start">Start confetti</button>
    <button @click="stop">Stop</button>
  </main>
</template>

<script>
  import Vue from 'vue'
  import VueConfetti from 'vue-confetti'

  Vue.use(VueConfetti)

  export default {
    methods: {
      startSteve() {
        this.$confetti.start({
          particles: [
            {
              type: 'image',
              size: 20,
              url: 'https://skypanel1.s3-eu-west-1.amazonaws.com/media_files/5cf6d33701062_Steve-Smiling.png',
              dropRate: 8
            }
          ]
        });
      },
      start() {
        this.$confetti.start();
      },
      stop() {
        this.$confetti.stop();
      },
    }
  }
</script>
