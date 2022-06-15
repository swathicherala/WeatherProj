<template>
  <div>
  <div id="main" :class="isDay ? 'day' : 'night'">
    <div class="container" style="max-width: 400px; min-width: 360px">
      <h1>Weather In</h1>
      <form v-on:submit.prevent="getWeather">
        <input type="text" v-model="citySearch" class="form-control" placeholder="What City?" />
      </form>
    </div>
    <p class="text-center my-3" v-if="cityFound">No city found</p>
      <div class="card rounded my-3 shadow-lg back-card overflow-hidden">
                <!-- weather animation container -->
        <div>
          <div icon="sunny" data-label="Sunny">
            <span class="sun"></span>
          </div>

          <div icon="snowy" data-label="Chilly">
           
          </div>

          <div icon="stormy" data-label="Soggy">
            <span class="cloud"></span>
            
          </div>
          <div icon="cloudy" data-label="Perfect">
            <span class="cloud"></span>
            <span class="cloud"></span>
          </div>
          <div icon="nightmoon" data-label="Cool!">
            <span class="moon"></span>
            <span class="meteor"></span>
          </div>
        </div>
        <!-- Top of card starts here -->
        <div class="card-top text-center" style="margin-bottom: 5rem">
          <div class="city-name my-3">
            <p>{{weather.cityName}}</p>
            <span>...</span>
            <p class="">{{weather.country}}</p>
          </div>
        </div>
        <!-- top of card ends here -->
        <!--card middle body, card body used cos I want to just update the innerHTML -->
        <div class="card-body">
          <!-- card middle starts here -->
          <div class="card-mid">
            <div class="row">
              <div class="col-12 text-center temp">
                <span>{{weather.temperature}}&deg;C</span>
                <p class="my-4">{{weather.description}}</p>
              </div>
            </div>
            <div class="row">
              <div class="col d-flex justify-content-between px-5 mx-5">
                <p>
                  <img src="" alt="" />
                  {{weather.lowTemp}}&deg;C
                </p>
                <p>
                  <img src="" alt="" />
                  {{weather.highTemp}}&deg;C
                </p>
              </div>
            </div>
          </div>
          <!-- card middle ends here -->

          <!-- card bottom starts here -->
          <div class="card-bottom px-5 py-4 row">
            <div class="col text-center">
              <p>{{weather.feelsLike}}&deg;C</p>
              <span>Feels like</span>
            </div>
            <div class="col text-center">
              <p>{{weather.humidity}}%</p>
              <span>humidity</span>
            </div>
          </div>

          <!-- card bottom ends here -->
      </div>
      </div>  
  </div>
   <div class="container">
    <h1>{{this.abcd}}</h1>
  </div>
  </div>
</template>

<script>
//import axios from 'axios'
export default{
  name:'App',
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
      const baseUrl=`https://api.openweathermap.org/data/2.5/weather?q=${this.citySearch}&appid=${key}&units=metric`
      
      const response=await fetch(baseUrl)
      const data=await response.json();
      console.log(data)
     
      this.weather.cityName=data.name
      this.weather.country=data.sys.country
      this.weather.temperature=data.main.temp
      this.weather.description=data.weather[0].description
      this.weather.lowTemp=data.main.temp_min
      this.weather.highTemp=data.main.temp_max
      this.weather.feelsLike=Math.round(data.main.feels_like)
      this.weather.humidity=data.main.humidity
       this.citySearch=""
       /*const key=`23db873f77msha7a5dff2e9f4038p18ed41jsn73d638e204a5`
       axios.get(`https://weather338.p.rapidapi.com/locations/search`)
       .then(response=>{
        console.log(response)
       })
      /* const options = {
  method: 'GET',
  url: 'https://weather338.p.rapidapi.com/weather/forecast',
  params: {
    date: '20200622',
    latitude: '37.765',
    longitude: '-122.463',
    language: 'en-US',
    units: 'm'
  },
  headers: {
    'X-RapidAPI-Key': '23db873f77msha7a5dff2e9f4038p18ed41jsn73d638e204a5',
    'X-RapidAPI-Host': 'weather338.p.rapidapi.com'
  }
};

axios.request(options).then(function (response) {
	console.log(response.data);
  const abcd=response.data
  console.log(abcd);
}).catch(function (error) {
	console.error(error);
});*/
    }
 }
}
</script>
<style>
#main {
  width: 35%;
  margin:auto;
}
.back-card {
  border-radius: 40px !important;
  color: white;
  background: linear-gradient(to bottom right, #707070, #434647);
  text-shadow: 2px 2px 2px #707070;
  
  text-align: center;
}
</style>
