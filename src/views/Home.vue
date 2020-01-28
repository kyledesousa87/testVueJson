<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>

    <GameRender/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import NavComp from '@/components/NavComp/NavComp.vue'
import GameRender from '@/components/GameRender/GameRender.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    NavComp,
    GameRender
  }
}
</script>
