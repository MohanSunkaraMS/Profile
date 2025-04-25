<template>
    <div class="bg-white shadow-md h-89 rounded-lg border">
      <h2 class="text-lg bg-gray-100 font-semibold text-gray-700 border-b p-2">
        Attendance Punch
      </h2>
  
      <div class="flex mt-4">
        <!-- Map Placeholder -->
        <img :src="mapImage" alt="Location Map" class="w-24 h-36 rounded-lg border w-[34%] ml-8 shadow-md">
  
        <!-- Punch Details -->
        <div class="ml-4">
          <h1 class="text-xl font-bold">{{ time }}</h1>
          <div class="flex justify-between ">
            <div>
              <p class="text-gray-600 mt-2">{{ day }}</p>
              <p class="text-gray-600 mt-2">{{ date }}</p>
            </div>
            <div class="mt-0 ml-14">
              <a href="#" class="text-blue-600 flex items-center space-x-1 hover:underline">
                <span>🌍 Web Check-In</span>
              </a>
              <a href="#" class="text-purple-600 flex items-center space-x-1 hover:underline mt-1">
                <span>🏡 Work from Home</span>
              </a>
            </div>
          </div>
        </div>
      </div>
  
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  const time = ref("HH:MM:SS");
  const day = ref("Tuesday");
  const date = ref("25, Feb 2025");
  const mapImage = ref("https://via.placeholder.com/100");
  </script>
  
  <style scoped>
  </style>
  