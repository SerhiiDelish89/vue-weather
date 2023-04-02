<template>
  <div class="widget">
    <div class="widget-head">
      <div class="widget-head_name" id="img"><img v-bind:src="'http://openweathermap.org/img/w/' + this.img + '.png'" /></div>
      <div class="widget-head_name" id="name">
        <span>{{ this.city }}</span>
      </div>
    </div>s
    <div class="w-widget_info"><span id="temp">{{this.temp}}</span>
    / feels like:
      <span id="feels">{{this.feels}}</span>
     
    </div>
    <div class="w-widget_info"><span id="description"></span></div>
    <div class="w-widget_info">humidity: <span id="humidity">{{ this.humidity }}</span>%</div>
    <FormWeather></FormWeather>
  </div>
</template>

<script>
import FormWeather from "./FormWeather.vue";
import axios from "axios";

export default {
  name: "WeatherWidget",
  components: {
    FormWeather,
  },
  data() {
    return {
      city: "",
      img: "",
      temp: "",
      feels: "",
      humidity: "",
    };
  },

  mounted() {
    axios
      .get(
        "https://api.openweathermap.org/data/2.5/weather?q=Sydney&units=metric&appid=0cf69d7b51047b5bd691266f2e26e463"
      )
      .then((response) => {
        (this.city = response.data.name), 
         (this.img = response.data.weather[0].icon)
        this.temp = response.data.main.temp
        this.feels = response.data.main.feels_like
        this.humidity = response.data.main.humidity
         console.log(response)
         console.log("")
      });
  },
};
</script>

<style lang="scss" scoped></style>
