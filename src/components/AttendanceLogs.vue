<template>
  <div class="p-0 h-fit justify-center">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 w-full">
      <!-- Attendance Summary Component -->
      <AttendanceSummary />

      <!-- Attendance Punch Component -->
      <AttendancePunch />
    </div>

    <!-- Full-width Attendance History Table -->
    <div class="mt-6 w-full">
      <AttendanceHistory />
    </div>

    <!-- Second Attendance Summary Component at the bottom -->
    <div class="mt-6 w-full">
      <AttendanceSummary1 />
    </div>
  </div>
</template>

<script setup>
import AttendanceSummary from "./attendance/AttendanceSummary.vue";
import AttendanceSummary1 from "./attendance/AttendanceSummary1.vue"; // ✅ Placed at the bottom
import AttendancePunch from "./attendance/AttendancePunch.vue";
import AttendanceHistory from "./attendance/AttendanceHistory.vue";
import LeaveSummary from "./attendance/LeaveSummary.vue";
</script>

<style scoped>
</style>