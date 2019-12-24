<template>
  <div class="home">
    {{ ENV_TEST }}
    <img alt="Vue logo" src="../assets/logo.png"/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  },
  data () {
    return {
      ENV_TEST: ''
    }
  },
  mounted () {
    this.ENV_TEST = process.env.VUE_APP_ENV_TEST
  }
}
</script>
