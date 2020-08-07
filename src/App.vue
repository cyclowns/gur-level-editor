<template>
  <div id="app">
    <div class="container">
      <Explorer/>
      <Properties/>
      <LevelView/>
    </div>
  </div>
</template>

<script>
import LevelView from './components/LevelView.vue'
import Explorer from './components/Explorer.vue'
import Properties from './components/Properties.vue'

export default {
  name: 'App',
  components: {
    LevelView,
    Explorer,
    Properties
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #ddd;
  background-color: #333;
  height: 100vh;
  width: 100vw;
}

.container {
  display: grid;
  grid-template-areas: "e l l"
                       "p l l";
  grid-template-rows: 1fr 1fr;
  grid-template-columns: 1fr 1fr 1fr;

  width: 100%;
  height: 100%;
}

#properties {
  grid-area: p;
}

#explorer {
  grid-area: e;
}

#levelview {
  grid-area: l;
}

</style>
