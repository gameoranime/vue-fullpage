<template>
  <div id="app">
    <full-page ref="fullpage" :options="options">
      <div class="section">
        
        <div class="slide"><h1>Section 3<button class="next" @click="$refs.fullpage.api.moveSectionDown()">Next</button></h1></div>
		<div class="slide"><h1>Slide 3.2</h1></div>
		<div class="slide"><h1>Slide 3.3</h1></div>
		<div class="slide"><h1>Slide 3.4</h1></div>
		<div class="slide"><h1>Slide 3.5</h1></div>
      </div>
      <div class="section">
        <button class="prev" @click="$refs.fullpage.api.moveSectionUp()">Prev</button>
        Section 2
      </div>
    </full-page>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld
  },
  data() {
    return {
      options: {
        menu: '#menu',
        anchors: ['page1', 'page2', 'page3'],
        sectionsColor: ['#41b883', '#ff5f45', '#0798ec'],
        scrollOverflow:true
      },
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
