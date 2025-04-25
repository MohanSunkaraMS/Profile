<template>
  <div class="bg-white shadow-md h-fit w-full rounded-lg border">
    
    <!-- Header Section -->
    <h2 class="bg-gray-100 text-md font-semibold p-4 rounded">Other Details</h2>

    <!-- Job Details Section -->
    <div class="mt-4 p-4">
      <h3 class="text-gray-700 font-semibold">Job Details</h3>
      <div class="grid gap-y-2 text-sm text-gray-600 mt-2">
        <div class="flex">
          <span class="w-40 text-[#898e90]">Employee ID:</span>
          <span>{{ jobDetails.employeeId }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Date Of Joining:</span>
          <span>{{ jobDetails.dateOfJoining }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Job Title:</span>
          <span>{{ jobDetails.jobTitle }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Work Type:</span>
          <span>{{ jobDetails.workType }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">In Probation:</span>
          <span>{{ jobDetails.inProbation || '-' }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Notice Period:</span>
          <span>{{ jobDetails.noticePeriod }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Contract Status:</span>
          <span>{{ jobDetails.contractStatus }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Shift:</span>
          <span>{{ jobDetails.shift }}</span>
        </div>
      </div>
    </div>

    <!-- Organization Level Section -->
    <div class="mt-6 p-4 ">
      <h3 class="text-gray-700 font-semibold">Organization Level</h3>
      <div class="grid gap-y-2 text-sm text-gray-600 mt-2">
        <div class="flex">
          <span class="w-40 text-[#898e90]">Company:</span>
          <span>{{ organization.company }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Department:</span>
          <span>{{ organization.department }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Reporting Manager:</span>
          <span class="text-blue-500 cursor-pointer">{{ organization.reportingManager }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">L2 Manager:</span>
          <span>{{ organization.l2Manager || '-' }}</span>
        </div>
      </div>
    </div>

    <!-- General Policies Section -->
    <div class="mt-6 p-4">
      <h3 class="text-gray-700 font-semibold">General Policies</h3>
      <div class="grid gap-y-2 text-sm text-gray-600 mt-2">
        <div class="flex">
          <span class="w-40 text-[#898e90]">Weekly Off Policy:</span>
          <span>{{ policies.weeklyOffPolicy || '-' }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Attendance Capture:</span>
          <span>{{ policies.attendanceCapture }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Attendance Penalization:</span>
          <span>{{ policies.attendancePenalization }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Leave Policy:</span>
          <span>{{ policies.leavePolicy }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Travel Policy:</span>
          <span>{{ policies.travelPolicy || '-Not Set-' }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Loan Policy:</span>
          <span>{{ policies.loanPolicy || '-Not Set-' }}</span>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  props: {
    jobDetails: Object,
    organization: Object,
    policies: Object,
  },
};
</script>
