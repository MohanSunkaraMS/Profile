<template>
  <div class="bg-white border rounded-lg shadow-md">
    <!-- Title -->
    <h2 class="text-lg font-semibold bg-gray-100 text-gray-700 border-b p-2">Leaves</h2>

    <div class="flex justify-between  p-4 items-center mt-4">
      <!-- Leave Summary -->
      <div class="flex space-x-8">
        <div v-for="(leave, index) in leaves" :key="index" class="text-center">
          <div class="relative w-24 h-24"> <!-- Increased container size -->
            <svg class="w-full h-full" viewBox="0 0 40 40"> <!-- Adjusted viewBox -->
              <!-- Background Circle -->
              <circle class="text-gray-200 stroke-gray-200" stroke-width="3" fill="transparent" r="18" cx="20"
                cy="20" />

              <!-- Progress Circle -->
              <circle stroke-width="3" fill="transparent" r="18" cx="20" cy="20" stroke-dasharray="100"
                :stroke-dashoffset="100 - leave.percentage" stroke-linecap="round" :class="leave.color" />
            </svg>
            <div class="absolute inset-0 flex flex-col justify-center items-center">
              <p class="text-sm font-medium">{{ leave.type }}</p>
              <p class="text-xs">{{ leave.days }} days</p>
            </div>
          </div>
        </div>


      </div>


      <!-- Links -->
      <div class="text-sm flex flex-col text-blue-600 space-y-2 text-right">
        <a href="#" class="hover:underline">Apply for leave</a>
        <a href="#" class="hover:underline">View all requests</a>
        <a href="#" class="hover:underline">View all balances</a>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const leaves = ref([
  { type: "Paid/Casual", days: 3, percentage: 30, color: "stroke-orange-400" },
  { type: "Paternity", days: 12, percentage: 75, color: "stroke-pink-400" },
  { type: "Unpaid", days: "∞", percentage: 100, color: "stroke-teal-400" }
]);
</script>

<style scoped>
svg {
  transform: rotate(-90deg);
}

circle {
  stroke-width: 3;
  fill: none;
  stroke-dasharray: 100;
  stroke-dashoffset: 0;
  transition: stroke-dasharray 0.5s ease-in-out;
}
</style>