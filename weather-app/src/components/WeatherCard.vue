<template>
  <div class="weather-card mt-4">
    <div class="topic">
      <div class="topic-title">City</div>
      <div class="topic-value">{{ location }}</div>
    </div>
    <hr>
    <div class="topic">
      <div class="topic-title">Weather Description</div>
      <div class="topic-value">{{ description }}</div>
    </div>
    <hr>
    <div class="topic">
      <div class="topic-title">Temperature</div>
      <div class="topic-value">{{ temperature }}°C</div>
    </div>
    <hr>
    <div class="topic">
      <div class="topic-title">Humidity</div>
      <div class="topic-value">{{ humidity }}%</div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      location: String,
      description: String,
      temperature: Number,
      humidity: Number,
    },
  };
</script>

<style>
  .weather-card {
    border: 1px solid #ddd;
    padding: 16px;
    margin: 16px 0;
  }
</style>