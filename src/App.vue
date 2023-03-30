<template>
  <TitleWeather></TitleWeather>
  <ContainerWeather>
  
</ContainerWeather>
</template>

<script>
import TitleWeather from "./components/TitleWeather.vue"
import ContainerWeather from './components/ContainerWeather.vue'

export default {
 name: "App",
 components:{
  TitleWeather,
  ContainerWeather ,
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
  margin-top: 60px;
}
</style>
