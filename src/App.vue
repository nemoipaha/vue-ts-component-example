<template>
  <div id="app">
    <div>
      <hello-component :msg="msg" :initialEnthusiasm="1" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';
import Hello from './components/Hello.vue'

@Component({
    components: {
        'hello-component': Hello
    }
})
export default class App extends Vue {
  msg: string = 'Welcome to Your Vue.js App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
