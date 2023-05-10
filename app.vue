<template>
  <div
    class="grid grid-cols-12 justify-center align-center relative fullscreen"
  >
    <div class="col-span-6 relative">
      <div class="absolute z-10">
        <h1 class="text-3xl text-white font-bold p-2">Workshop Weather</h1>
      </div>

      <div class="absolute m-auto left-0 right-0 z-10">
        <div class="pt-64">
          <div class="text-center">
            <h2 class="text-2xl font-semibold text-white">
              The Only Weather Forcast You Need
            </h2>

            <div class="h-1 bg-blue-400 w-24 mt-2 mx-auto" />

            <div class="mt-10 mx-64">
              <input
                @change="OnSearchInput($event)"
                class="bg-white/50 text-black placeholder-black/75 border border-gray-300 text-md rounded-lg font-semibold focus:ring-blue-400 focus:border-blue-400 block w-full p-2.5"
                type="text"
                placeholder="Enter Location"
              />
            </div>
          </div>
        </div>
      </div>

      <div class="bg-black fullscreen absolute">
        <img
          class="object-cover fullscreen opacity-75"
          src="https://res.cloudinary.com/dxns0vltg/image/upload/v1683707257/beautiful-nature-wallpaper_rgihvy.jpg"
        />
      </div>
    </div>
    <!-- Create a weather -->
    <div class="col-span-6 self-center mb-64" v-if="data.location != ''">

      <h1 class="text-3xl font-bold mx-20 p-5">Weather Today</h1>
      
      <div class="bg-white rounded-md mx-20 p-5">
        <div class="grid grid-cols-12">
          <div class="col-span-6">
            <!-- Celcius -->
            <h3 class="text-3xl font-bold">℃</h3>

            <div class="flex items-center">
              <!-- Condition -->
              <p class="text-2xl"></p>
              <!-- Image Condition -->
              <img class="h-20 w-20" :src="data.image" />
            </div>
            	
            <!-- Formatted Date Time -->
            <p class="font-semibold"></p>
          </div>

          <div class="col-span-6 border-2 border-white border-l-blue-400">
            <div class="px-5 font-semibold">
              <p>Feels Like: ℃</p>

              <p>Humidity: %</p>
              
              <p>Wind:  kph </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
body {
  background-color: #f5f4f4;
}
.fullscreen {
  height: 100vh;
}
</style>

<script setup lang="ts">
// Date-fns is a library that helps with formatting dates in javascript
import { format } from "date-fns";
// This is the API key for the weather API url https://www.weatherapi.com/docs/
const apikey = "f2a85c93126d4ccf85a173821211712";

// Step 1: Create a reactive object called data with the following properties 
// celcius, image, location, condition, feelslike, humidity, wind, winddir, date


// Step 2: Create a function called OnSearchInput that takes in an event as a parameter


// Step 3: Create a function called fetchWeather that takes in a string as a parameter


// Step 4: Create a function called setWeather that takes in an object as a parameter


// Bonus: Use IP Address to get a weather forecast for the user's location with the following API https://ipapi.co/
</script>
