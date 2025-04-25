<template>
    <div class="w-1/4 bg-white p-4 rounded shadow-md">
      <h3 class="font-semibold mb-2">February</h3>
      <div class="grid grid-cols-7 gap-1 text-center text-sm">
        <span v-for="day in days" :key="day" class="p-1">{{ day }}</span>
      </div>
      <div class="grid grid-cols-7 gap-1 mt-2 text-center">
        <span v-for="(date, index) in dates" :key="index"
          :class="['p-2 rounded-full', selectedDates.includes(date) ? 'bg-purple-300' : '']">
          {{ date }}
        </span>
      </div>
      <hr class="border-t-4 w-[107%] border-gray-300 my-4">
      
      <div class="mt-4">
        <h4 class="font-semibold">Legend</h4>
        <ul>
          <li class="flex items-center gap-2"><span class="w-4 h-4 bg-purple-400 rounded-full"></span> Present</li>
          <li class="flex items-center gap-2"><span class="w-4 h-4 bg-green-200 rounded-full"></span> Paid Leave</li>
          <li class="flex items-center gap-2"><span class="w-4 h-4 bg-yellow-200 rounded-full"></span> Unpaid Leave</li>
          <li class="flex items-center gap-2"><span class="w-4 h-4 bg-red-200 rounded-full"></span> Week Off</li>
          <li class="flex items-center gap-2"><span class="w-4 h-4 bg-blue-200 rounded-full"></span> Holiday</li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      selectedDates: Array
    },
    data() {
      return {
        days: ['M', 'T', 'W', 'T', 'F', 'S', 'S'],
        dates: Array.from({ length: 28 }, (_, i) => i + 1)
      };
    }
  };
  </script>
  