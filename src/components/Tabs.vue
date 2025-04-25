<script setup>
import { ref, shallowRef, defineAsyncComponent } from "vue";

// Import components dynamically
const components = {
  "Personal Details": defineAsyncComponent(() => import("./PersonalDetails.vue")),
  "Attendance Logs": defineAsyncComponent(() => import("./AttendanceLogs.vue")),
  "Leave Logs": defineAsyncComponent(() => import("./LeaveLogs.vue")),
  "My Payroll": defineAsyncComponent(() => import("./MyPayroll.vue")),
  "Tax Management": defineAsyncComponent(() => import("./TaxManagement.vue")),
};

const tabs = Object.keys(components);
const activeTab = ref(tabs[0]);
const activeComponent = shallowRef(components[activeTab.value]);

const selectTab = (tab) => {
  activeTab.value = tab;
  activeComponent.value = components[tab];
};
</script>

<template>
<!-- <div class="w-[193%] ml-[110px]"> -->
  <!-- Adjusted width to 80% -->
    <!-- Tabs -->
    <div class="absolute top-0 left-0 w-[78%] ml-12">



    <div class="flex border-b">
      <button
        v-for="tab in tabs"
        :key="tab"
        @click="selectTab(tab)"
        class="py-2 px-4 text-sm font-medium focus:outline-none"
        :class="activeTab === tab ? 'text-black border-b-2 border-blue-500 font-semibold' : 'text-gray-400'"
      >
        {{ tab }}
      </button>
    </div>

    <!-- Render Selected Tab Component -->
    <div class="mt-4">
      <component :is="activeComponent" />
    </div>
  </div>
</template>
