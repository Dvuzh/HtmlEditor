<template>
  <div id="app">    
    <LeftMenu />
    <Main />
    <MainTable />
  </div>
</template>

<script>
import Main from'./components/Main'
import LeftMenu from './components/LeftMenu'
import Vue from 'vue'
import VueDraggable from 'vue-draggable'
import MainTable from './components/MainTable'

Vue.use(VueDraggable)

export default {
  name: 'app',
  components: {
    Main,
    LeftMenu,
    MainTable
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
