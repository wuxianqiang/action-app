<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld @check="handlecheck" msg="Hello Vue 3.0 + Vite" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  setup (props) {
    const handlecheck = () => {
      console.log('todo')
    }
    return {
      HelloWorld,
      handlecheck
    }
  }
}
</script>
