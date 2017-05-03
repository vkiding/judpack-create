<template>
  <div class="wrapper" @click="update">
    <image :src="logoUrl" class="logo"></image>
    <text class="title">Hello {{target}}</text>
    <text class="desc">Now, let's use vue to build your jud app.</text>
  </div>
</template>

<style>
  .wrapper { align-items: center; margin-top: 120px; }
  .title { padding-top:40px; padding-bottom: 40px; font-size: 48px; }
  .logo { width: 360px; height: 156px; }
  .desc { padding-top: 20px; color:#888; font-size: 24px;}
</style>

<script>
  export default {
    data: {
      logoUrl: 'https://raw.githubusercontent.com/vkiding/jud-toolkit/master/jud.png',
      target: 'World'
    },
    methods: {
      update: function (e) {
        this.target = this.target === 'Jud' ? 'World' : 'Jud'
        console.log('target:', this.target)
      }
    }
  }
</script>