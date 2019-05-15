<template>
  <div id="app">
    <div class="bkg" v-bind:style="{background:customBkg}">
      <!--<img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App"/>-->

      <!--binding dynamicaly-->
      <h2 v-bind:class="{active: activeBkg}">I am a heading</h2>
      <a v-bind:href="link">A Website</a>

      <h1 v-bind:style="{color:customColor}">Dynamic Styling is Cool</h1>
      <input type="text" placeholder="Enter a color" v-model="customColor">
      <input type="text" placeholder="Enter a background color" v-model="customBkg">
    </div>
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
      link: "https://www.youtube.com",
      activeBkg: false,
      customColor: "",
      customBkg: ""
    };
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  height: 100vh;
}

.active {
  background: lightcoral;
  color: white;
}

.bkg {
  height: 100vh;
}
</style>
