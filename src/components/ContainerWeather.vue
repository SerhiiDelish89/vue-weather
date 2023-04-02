<template>
    <div class="container">
<slot>Default value</slot>
<WeatherWidget></WeatherWidget>
    </div>
</template>

<script>
import WeatherWidget from './WeatherWidget.vue'

    export default {
        name: 'ContainerWeather',
        components:{
            WeatherWidget,
        }
    }
</script>

<style lang="css" scoped>
 .container{
     max-width: 450px;
    margin: 0 auto;
    background-color: cornflowerblue;
    border: 2px solid;
    border-radius: 10px;
 }
</style>