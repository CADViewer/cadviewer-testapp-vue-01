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

// NOTE:  IF YOU IN INDEX.HTML ADD IN CADVIEWER CLASS DECLARATIONS FROM /PUBLIC/CADVIEWER_TOPLEVEL_VUE/APP/.. then the components _no_npm can be used.

// Standard use
import CADViewerCanvas from './components/CADViewerCanvas.vue'    // STANDARD NPM INSTALL
import CADViewerHelperMethods from './components/CADViewerHelperMethods.vue' // STANDARD NPM INSTALL
import CADViewerSpaceObjects from './components/CADViewerSpaceObjects.vue' // STANDARD NPM INSTALL

// Altenative use, see index.html for import of CADViewer and jQuery
/*
import CADViewerCanvas from './components/CADViewerCanvas_no_npm.vue'   // NO NPM INSTAL - GLOBAL use cadviewer_toplevel_vue - not recommended
import CADViewerHelperMethods from './components/CADViewerHelperMethods_no_npm.vue' // NO NPM INSTAL - GLOBAL use cadviewer_toplevel_vue - not recommended
import CADViewerSpaceObjects from './components/CADViewerSpaceObjects_no_npm.vue' // NO NPM INSTAL - GLOBAL use cadviewer_toplevel_vue - not recommended
*/

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
