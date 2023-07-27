<template>
  <div class="app">
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container" style= "border: none; padding: 0px;">
        <a class="navbar-brand">Weather App</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ml-auto">
            <li class="nav-item">
              <a class="nav-link" href="#" onclick="location.reload();">Home</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <div class="container">
      <h1 class="mt-4">Real-Time Weather Application</h1>
      <WeatherForm @weatherData="setWeatherData" />
      <WeatherCard
        v-if="weatherData"
        :location="weatherData.name"
        :description="weatherData.weather[0].description"
        :temperature="weatherData.main.temp"
        :humidity="weatherData.main.humidity"
      />
    </div>
  </div>
</template>

<style>
  .container {
    max-width: 600px;
    margin: 20px auto;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }

  .city-description {
    margin-top: 20px;
    font-style: italic;
  }

  .topic-title {
    font-size: 18px;
    font-weight: bold;
    margin-top: 20px;
  }

  .topic-value {
    font-size: 16px;
    margin-top: 10px;
  }
  .topic-value::first-letter {
    text-transform: uppercase;
  }

  .topic {
    margin-bottom: 20px;
  }
</style>

<script>
  import WeatherForm from "@/components/WeatherForm.vue";
  import WeatherCard from "@/components/WeatherCard.vue";

  export default {
    components: {
      WeatherForm,
      WeatherCard,
    },
    data() {
      return {
        weatherData: null,
      };
    },
    methods: {
      setWeatherData(data) {
        this.weatherData = data;
      },
    },
  };
</script>