<template>
  <div class="bg-white shadow-md rounded-lg border">
    <h2 class="text-lg font-semibold bg-gray-100 text-gray-700 border-b p-2">
      Attendance History
    </h2>

    <div class="overflow-x-auto p-4 mt-4">
      <table class="w-full border-collapse">
        <thead>
          <tr class="bg-gray-800 text-white  rounded-lg text-left">
            <th class="p-3">Request on</th>
            <th class="p-3">Request type</th>
            <th class="p-3">Applicable Date</th>
            <th class="p-3">Note</th>
            <th class="p-3">Status</th>
            <th class="p-3">Last Action</th>
            <th class="p-3">Approver</th>
            <th class="p-3">Actions</th>
          </tr>
        </thead>

        <tbody>
          <tr v-for="(record, index) in attendanceRecords" :key="index" class="border-b hover:bg-gray-100">
            <td class="p-3">
              <p class="text-gray-700">{{ record.requestOn }}</p>
              <p class="text-gray-500 text-sm">by {{ record.user }}</p>
            </td>
            <td class="p-3">{{ record.requestType }}</td>
            <td class="p-3">
              <p>{{ record.applicableDate }}</p>
              <p class="text-blue-600 text-sm hover:underline cursor-pointer">📌 {{ record.timeIn }}</p>
              <p class="text-blue-600 text-sm hover:underline cursor-pointer">⏳ {{ record.timeOut }}</p>
            </td>
            <td class="p-3">{{ record.note }}</td>
            <td class="p-3">
              <span class=" px-2 py-1 rounded-md text-sm">
                {{ record.status }}
              </span>
            </td>
            <td class="p-3">{{ record.lastAction }}</td>
            <td class="p-3">{{ record.approver }}</td>
            <td class="p-3  space-x-4 text-blue-600">

             
              <button class="p-2 rounded hover:text-green-600">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 fill-current text-gray-600 hover:text-green-600"
                  viewBox="0 0 384 512">
                  <!-- Font Awesome Free 6.7.2 -->
                  <path
                    d="M215.7 499.2C267 435 384 279.4 384 192C384 86 298 0 192 0S0 86 0 192c0 87.4 117 243 168.3 307.2c12.3 15.3 35.1 15.3 47.4 0zM192 128a64 64 0 1 1 0 128 64 64 0 1 1 0-128z" />
                </svg>
              </button>
              <button class="p-2 rounded hover:text-red-600">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 fill-current text-gray-600 hover:text-red-600"
                  viewBox="0 0 448 512">
                  <!-- Font Awesome Free 6.7.2 -->
                  <path
                    d="M135.2 17.7C140.6 6.8 151.7 0 163.8 0L284.2 0c12.1 0 23.2 6.8 28.6 17.7L320 32l96 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 96C14.3 96 0 81.7 0 64S14.3 32 32 32l96 0 7.2-14.3zM32 128l384 0 0 320c0 35.3-28.7 64-64 64L96 512c-35.3 0-64-28.7-64-64l0-320zm96 64c-8.8 0-16 7.2-16 16l0 224c0 8.8 7.2 16 16 16s16-7.2 16-16l0-224c0-8.8-7.2-16-16-16zm96 0c-8.8 0-16 7.2-16 16l0 224c0 8.8 7.2 16 16 16s16-7.2 16-16l0-224c0-8.8-7.2-16-16-16zm96 0c-8.8 0-16 7.2-16 16l0 224c0 8.8 7.2 16 16 16s16-7.2 16-16l0-224c0-8.8-7.2-16-16-16z" />
                </svg>
              </button>

              <button v-if="record.hasLocation" class="p-2 rounded hover:text-blue-600">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 fill-current text-gray-600 hover:text-blue-600"
                  viewBox="0 0 512 512">
                  <!-- Font Awesome Free 6.7.2 -->
                  <path
                    d="M362.7 19.3L314.3 67.7 444.3 197.7l48.4-48.4c25-25 25-65.5 0-90.5L453.3 19.3c-25-25-65.5-25-90.5 0zm-71 71L58.6 323.5c-10.4 10.4-18 23.3-22.2 37.4L1 481.2C-1.5 489.7 .8 498.8 7 505s15.3 8.5 23.7 6.1l120.3-35.4c14.1-4.2 27-11.8 37.4-22.2L421.7 220.3 291.7 90.3z" />
                </svg>
              </button>




            </td>

          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const attendanceRecords = ref([
  {
    requestOn: "24 Feb, 2025 07:00:56",
    user: "Devashish Bariko",
    requestType: "Regularization",
    applicableDate: "11 Feb, 2025",
    timeIn: "09:28:53",
    timeOut: "10:20:16",
    note: "Missed login",
    status: "Pending",
    lastAction: "Updated by Devashish",
    approver: "Anvitha Reddy",
    hasLocation: true,
  },
  {
    requestOn: "28 Feb, 2025",
    user: "Devashish Bariko",
    requestType: "Clock In - Regular",
    applicableDate: "28 Feb, 2025",
    timeIn: "09:15:23",
    timeOut: "Missing",
    note: "In",
    status: "Pending",
    lastAction: "Request by Devashish",
    approver: "Anvitha Reddy",
    hasLocation: false,
  },
  {
    requestOn: "24 Feb, 2025 07:00:56",
    user: "Devashish Bariko",
    requestType: "Clock In - Remote",
    applicableDate: "11 Feb, 2025",
    timeIn: "09:28:53",
    timeOut: "10:20:16",
    note: "Missed login",
    status: "Pending",
    lastAction: "Updated by Devashish",
    approver: "Anvitha Reddy",
    hasLocation: true,
  },
  {
    requestOn: "24 Feb, 2025 07:00:56",
    user: "Devashish Bariko",
    requestType: "Work from home",
    applicableDate: "11 Feb, 2025",
    timeIn: "09:28:53",
    timeOut: "10:20:16",
    note: "Family emergency",
    status: "Pending",
    lastAction: "Updated by Devashish",
    approver: "Anvitha Reddy",
    hasLocation: false,
  }
]);
</script>

<style scoped>
table {
  border: 1px solid #ddd;
  border-collapse: collapse;
  /* Ensures borders don't double up */
  width: 100%;
}

th,
td {
  text-align: left;
  padding: 10px;
  border: 1px solid #ddd;
  /* Adds border to each cell */
}
</style>