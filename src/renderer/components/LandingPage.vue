<template>
  <div class="container">
    <div class="row header-logo">
      <div class="col d-flex justify-content-center align-items-center">
        <img id="logo" src="~@/assets/pipe-96.png" alt="electron-vue">
        <div>
          <p class="app-title">Bulking Conversion App</p>
          <p class="app-sub">Simple App to mass shorten urls</p>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="cold col-md-8 d-flex flex-column justify-content-start">
        <router-link :to="{name: 'create-project'}">
          <big-button faName="fa-plus-circle" text="Create new"></big-button>
        </router-link>
      </div>
      <div class="col col-md-4">
        <head-title title="Last Projects" faName="fa-clock-o"></head-title>
        <ul>
          <li>Project 1</li>
          <li>Project 2</li>
        </ul>
      </div>
    </div>
    <div class="row d-flex justify-content-center">
      <author></author>
    </div>
  </div>
</template>

<script>
  import Author from './Utilities/Author'
  import HeadTitle from './Utilities/HeadTitle'
  import BigButton from './Utilities/BigButton'
  
  export default {
    name: 'landing-page',
    components: { Author, HeadTitle, BigButton },
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body { font-family: 'Source Sans Pro', sans-serif; }

  .container {
    height: 100vh;
    padding: 30px 10px;
  }

  .header-logo {
    margin-bottom: 50px;
  }

  .app-title, .app-sub {
    margin-bottom: 0;
  }
  .app-title {
    font-size: 25px;
    font-weight: bold;
    color: #0098ed;
  }

  .app-sub {
    color: #2f56af;
  }

  .main-content {
    min-width: w;
  }
</style>
