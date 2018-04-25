<template>
  <div class="wrapper">
    <image :src="logo" class="logo" />
    <text class="greeting">The environment is ready!</text>
    <button @click="goTo('/todo')">HELLO</button>
    <div style="height: 600px; width: 600px">
      <router-view/>
    </div>
  </div>
</template>

<script>
import router from './router'
export default {
  name: 'App',
  data () {
    return {
      logo: 'https://gw.alicdn.com/tfs/TB1yopEdgoQMeJjy1XaXXcSsFXa-640-302.png'
    }
  },
  methods: {
    goTo (page) {
      router.push(page)
    }
  }
}
</script>

<style scoped>
  .wrapper {
    justify-content: start;
    align-items: center;
  }
  .logo {
    width: 200px;
    height: 100px;
  }
  .greeting {
    text-align: center;
    font-size: 20px;
    color: #41B883;
  }
  .message {
    margin: 30px;
    font-size: 32px;
    color: #727272;
  }
</style>
