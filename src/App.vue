<template>
  <div id="app">
  <!--<img src="./assets/LM-logo.png" alt="LM">-->
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/findMe">Send location</router-link></li>
    </ul>
    <router-view/>
  </div>
</template>

<script>
import Home from './components/Home.vue'
import Geolocation from './components/Geolocation'
import sFooter from './components/sFooter.vue'
import sHeader from './components/sHeader'
export default {
  components:{
     sHeader,
     Home ,
    Geolocation,
     sFooter
  },
  data(){
    return{
     
    }
  }
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
li{
  list-style-type: none;
  display: inline;
}
</style>
