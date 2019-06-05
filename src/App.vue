<template>
  <div id="app">
    <Header v-bind:searchPhoto="searchPhoto" />
    <Photos v-bind:photos="photos" />
  </div>
</template>

<script>
import Header from './components/layout/Header';
import Photos from './components/Photos';
import axios from 'axios';

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    background: url('./assets/stars.gif');
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }

  .btn {
    display: inline-block;
    border: none;
    background: #1CB76F;
    color: #fff;
    padding: 7px 20px;
    cursor: pointer;
  }

  .btn:hover {
    opacity: .9;
  }
</style>
