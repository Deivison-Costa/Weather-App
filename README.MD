# Weather App

- The Weather App is a real-time weather application built using Vue.js. It allows users to check the weather information of a specific location. 
- Users can enter the name of a city and get the current weather details, including temperature and humidity.

# Installation and Setup
## Clone the repository to your local machine using the following command:
    git clone https://github.com/Deivison-Costa/Weather-App
## Navigate to the project directory:
    cd weather-app
## Install the required dependencies using npm or yarn:
    npm install
## Create a free account on OpenWeatherMap and get an API key. 
    const response = await axios.get(
        `https://api.openweathermap.org/data/2.5/weather?q=${this.location}&units=metric&appid=YOUR_API_KEY`
    );

- https://openweathermap.org/api
- Replace YOUR_API_KEY in src/components/WeatherForm.vue with your actual API key.
## Install the required dependencies:
- **Vue.js**: A progressive JavaScript framework for building user interfaces.
- **Axios**: A promise-based HTTP client for making API requests.
- **Bootstrap**: A popular CSS framework for creating responsive and mobile-first websites.

# Usage
## To start the application, run the following command in the project directory:
    npm run serve
- The application will open in your default web browser at http://localhost:8080.
- Once the application is running, open it in your web browser. You will see the Weather App interface with a navigation bar at the top and a form to enter the city's name. 
- Type the name of the city you want to check the weather for and click the "Get Weather" button.
- The application will fetch the weather information from the OpenWeatherMap API and display the city name, weather description, temperature, and humidity on the Weather Card below the form.

# Features
- Real-time weather information for a specific city.
- User-friendly interface.
- Easy to use and responsive design.

# Technology Stack
- Vue.js;
- Axios;
- Bootstrap.
