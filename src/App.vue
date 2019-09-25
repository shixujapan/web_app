<template>
    <div id="app">
      <displaymain></displaymain>
    </div>
  </template>
  
  <script>
  import displaymain from './components/display_main.vue'
  
  export default {
    name: 'app',
    components: {
      displaymain
    }
  }
  </script>
  
  <style >
  #app {
    width: 1200px;
    height: 900px;
    margin: auto;
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    border-radius: 10px;
    border: rgb(204, 232, 255) solid 2px;
    background: rgb(204, 232, 255);
  }
  </style>