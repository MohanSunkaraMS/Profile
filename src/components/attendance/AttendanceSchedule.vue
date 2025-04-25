<template>
    <div class="flex-1">
      <div class="flex justify-between gap-4">
        <div class="flex justify-between items-center mb-4">
          <h4 class="text-2xl text-center mr-2 ml-4 font-semibold leading-[3rem]">
            22-28 February 2024
          </h4>
          <select class="border rounded p-1 text-gray-600">
            <option>Weekly</option>
          </select>
        </div>
  
        <div class="flex items-center space-x-6">
          <label class="flex items-center space-x-2">
            <input type="checkbox" checked class="form-checkbox text-purple-600" />
            <span>Attendance log</span>
          </label>
          <label class="flex items-center space-x-2">
            <input type="checkbox" class="form-checkbox text-purple-600" />
            <span>Leave log</span>
          </label>
        </div>
      </div>
      <hr class="border-t-4 w-[103%] border-gray-300 my-4">
  
      <div class="flex mt-4">
        <div class="w-16 border-r border-gray-300 text-right pr-2">
          <div v-for="hour in hours" :key="hour"
            class="h-16 flex items-center justify-end text-gray-600 text-sm">
            {{ hour }}
          </div>
        </div>
  
        <div class="flex-1 grid grid-cols-7 gap-0 border-t border-l border-gray-300">
          <div v-for="day in week" :key="day" class="border-r border-gray-300 relative">
            <h4 class="text-center font-medium py-2 bg-gray-100">{{ day }}</h4>
            <div v-for="hour in hours" :key="hour" class="h-12 border-b border-gray-300 relative">
              <div v-if="(day === 'Monday' && hour === '09:00') || (day === 'Tuesday' && hour === '10:00')"
                class="w-6 bg-purple-400 h-8 absolute left-1/2 transform -translate-x-1/2">
              </div>
            </div>
            <div v-if="['Thursday', 'Friday', 'Saturday'].includes(day)"
              class="absolute inset-0 bg-purple-100 opacity-30 pointer-events-none">
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        week: ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday'],
        hours: ['09:00', '10:00', '11:00', '12:00', '13:00', '14:00']
      };
    }
  };
  </script>
  
  <style scoped>
  .form-checkbox {
    width: 1rem;
    height: 1rem;
  }
  </style>
  