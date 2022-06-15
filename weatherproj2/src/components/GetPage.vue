<template>
  <div class="main">
    <div class="container text-center" style="max-width:400px;">
       <h1 class="mb-4">Weather Report</h1>
       <form class="mb-4" v-on:submit.prevent="getWeather">
        <input type="text" v-model="citySearch" class="form-control" placeholder="City Name"/>
       </form>
       <div class="card" style="background-color:#99ccff;height:250px">
           <span>City Name:</span>
           <p>{{weather.cityName}}</p>
           <p>Country:{{weather.country}}</p>
       </div>
    </div>
  </div>
</template>

<script>

import axios from 'axios'
export default {
  name: 'GetPage',
  data(){
       return{
        citySearch:"",
        weather:{
        cityName: "Gwarinpa",
        country: "NG",
        temperature: 12,
        description: "Clouds everywhere",
        lowTemp: "19",
        highTemp: "30",
        feelsLike: "20",
        humidity: "55",
       }
    }
  },
  methods:{
    async getWeather(){
    console.log(this.citySearch)
    const key="4d70d5f47bcb26e93ff1788570b78de8"
    axios.get(`https://api.openweathermap.org/data/2.5/weather?q=${this.citySearch}&appid=${key}&units=metric`)
    .then(response=>{
      this.citySearch=response 
      console.log(response)
    })
    console.log("data",this.citySearch)
      const data=await this.citySearch
      this.weather.cityName=data.name
      this.weather.country=data.sys.country
      this.weather.temperature=data.main.temp
      this.weather.description=data.weather[0].description
      this.weather.lowTemp=data.main.temp_min
      this.weather.highTemp=data.main.temp_max
      this.weather.feelsLike=Math.round(data.main.feels_like)
      this.weather.humidity=data.main.humidity
       this.citySearch=""
  }
 }
}
</script>

<style>

</style>
