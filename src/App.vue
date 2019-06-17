<template>
  <div id="app">    
    <LeftMenu />
    <Main />
  </div>
</template>

<script>
import Main from'./components/Main'
import LeftMenu from './components/LeftMenu'


export default {
  name: 'app',
  components: {
    Main,
    LeftMenu,
    // draggable
  }
}
</script>

<style>
#app {
    height: 100%;
    overflow: hidden;
    display: flex;
    align-items: center;
    padding: 0;
  }
</style>
