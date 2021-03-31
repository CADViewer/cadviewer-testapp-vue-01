<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" width="40px">
    <app-helloworld msg="Welcome to Your Vue.js App"></app-helloworld>
    <app-cadviewerhelpermethods ref="cadviewerhelpermethods"></app-cadviewerhelpermethods>
    <app-cadviewerspaceobjects ref="cadviewerspaceobjects"></app-cadviewerspaceobjects>
    <app-cadviewercanvas ref="cadviewercanvas"></app-cadviewercanvas>

    
  </div>
</template>


<script>
import HelloWorld from './components/HelloWorld.vue'
import CADViewerCanvas from './components/CADViewerCanvas.vue'
import CADViewerHelperMethods from './components/CADViewerHelperMethods.vue'
import CADViewerSpaceObjects from './components/CADViewerSpaceObjects.vue'


export default {
  name: 'App',
  components: {
    'app-helloworld': HelloWorld,
    'app-cadviewerhelpermethods' : CADViewerHelperMethods,
    'app-cadviewerspaceobjects' : CADViewerSpaceObjects,
    'app-cadviewercanvas': CADViewerCanvas,
  }
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
}
</style>
