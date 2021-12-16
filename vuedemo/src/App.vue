<template>
  <div id="app">
    <header class="appHeader">
    <appHeader />
    </header>
    <div class="selectBox">
      <appSelect />
    </div>
    <main class="mainBox"></main>
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/imgShow">imgShow</router-link>
    </div> -->
    <!-- <router-view /> -->
  </div>
</template>

<script>
// @ is an alias to /src
import appHeader from '@/components/appHeader/appHeader.vue'
import appSelect from '@/components/appSelect/appSelect.vue'

export default {
  name: 'Home',
  components: {
    appHeader,
    appSelect
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* width: 100%;
  height: 100%;
  background: url(../src/assets/img/dongzhi.jpg) no-repeat;
  background-size: 100% 100%; */
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
.selectBox {
  /* padding-top: 30px; */
}
</style>
