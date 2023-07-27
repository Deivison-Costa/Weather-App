<template>
  <div class="weather-form mt-4">
    <input
      type="text"
      class="form-control"
      v-model="location"
      placeholder="Enter a location"
    />
    <button @click="getWeather" class="btn btn-dark mt-2">Get Weather</button>
  </div>
</template>

<script>
  import axios from "axios";

  export default {
    data() {
      return {
        location: "",
      };
    },
    methods: {
      async getWeather() {
        try {
          const response = await axios.get(
            `https://api.openweathermap.org/data/2.5/weather?q=${this.location}&units=metric&appid=YOUR_API_KEY`
          );
          this.$emit("weatherData", response.data);
        } catch (error) {
          console.error(error);
        }
      },
    },
  };
</script>

<style>
  .weather-form {
    margin: 16px 0;
  }
</style>
