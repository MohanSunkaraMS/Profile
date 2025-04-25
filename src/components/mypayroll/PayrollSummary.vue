<template>
    <div class="border border-gray-300 rounded-lg shadow-md">

      <h2 class="text-sm bg-gray-100 rounded-t-lg p-2   font-semibold border-b pl-4">
        Payroll Summary
      </h2>
      <div class="mt-3 grid grid-cols-2 gap-x-1 gap-y-0 p-2 text-sm text-gray-700">
        <div class="w-full pr-1">
          <div class="flex py-1">
            <span class="font-medium text-gray-600 w-1/3">Payroll Cycle:</span>
            <span class="font-semibold w-2/3">{{ payroll.cycle }}</span>
          </div>
          <div class="flex py-1">
            <span class="font-medium text-gray-600 w-1/3">Current Compensation:</span>
            <span class="font-semibold w-2/3">{{ payroll.compensation }} <span class="text-xs font-normal">/ Annual</span></span>
          </div>
          <div class="flex py-1">
            <span class="font-medium text-gray-600 w-1/3">Last Processed Cycle:</span>
            <span class="font-semibold w-2/3">{{ payroll.lastCycle }}</span>
          </div>
        </div>
        <div class="w-full pl-1">
          <div class="flex py-1">
            <span class="font-medium text-gray-600 w-1/3">Current Process Cycle:</span>
            <span class="font-semibold w-2/3">{{ payroll.processCycle }}</span>
          </div>
          <div class="flex py-1">
            <span class="font-medium text-gray-600 w-1/3">Working Days:</span>
            <span class="font-semibold w-2/3">{{ payroll.workingDays }} Days</span>
          </div>
          <div class="flex py-1">
            <span class="font-medium text-gray-600 w-1/3">Loss of Pay:</span>
            <span class="font-semibold w-2/3">{{ payroll.lossOfPay }} Days</span>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: ["payroll"],
  };
  </script>
  