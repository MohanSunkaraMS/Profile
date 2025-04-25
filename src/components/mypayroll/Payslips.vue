<template>
    <div class="flex flex-col mr-[30%]">
      <div class="bg-gray-100 w-[175%] p-4 shadow-sm">
        <div class="max-w-10xl flex gap-4">
          <h2 class="text-lg font-semibold text-gray-800">Payslips</h2>
          <select v-model="selectedYear" class="border rounded-md px-3 py-1 text-gray-700">
            <option v-for="year in years" :key="year" :value="year">{{ year }}</option>
          </select>
          <select v-model="selectedMonth" class="border rounded-md px-3 py-1 text-gray-700">
            <option v-for="month in months" :key="month" :value="month">{{ month }}</option>
          </select>
        </div>
      </div>
      <div class="w-full w-[175%]  bg-white shadow-lg border-[16px] border-gray-600 ">


        <div class="p-6 text-gray-800">
          <div class="p-6 text-black text-center rounded-t-lg">
            <h1 class="text-2xl font-bold">INDOSOL</h1>
            <p class="text-sm">Consultant Payslip - {{ payroll.processCycle }}</p>
          </div>
  
          <h2 class="text-lg font-semibold border-b pb-1 mt-0 mb-3">Employee Details</h2>
          <p><strong>Name:</strong> {{ payroll.employee.name }}</p>
          <p><strong>Employee ID:</strong> {{ payroll.employee.id }}</p>
          <p><strong>Designation:</strong> {{ payroll.employee.designation }}</p>
          <p><strong>Department:</strong> {{ payroll.employee.department }}</p>
          <p><strong>Date of Joining:</strong> {{ payroll.employee.doj }}</p>
          <p><strong>Work Location:</strong> {{ payroll.employee.location }}</p>
  
          <h2 class="text-lg font-semibold border-b pb-1 mt-4 mb-3">Salary Details</h2>
          <p><strong>Basic Salary:</strong> INR {{ payroll.salary.basic }}</p>
          <p><strong>HRA:</strong> INR {{ payroll.salary.hra }}</p>
          <p><strong>Conveyance Allowance:</strong> INR {{ payroll.salary.conveyance }}</p>
          <p><strong>Other Allowances:</strong> INR {{ payroll.salary.allowances }}</p>
          <p class="font-bold mt-2"><strong>Gross Salary:</strong> INR {{ payroll.salary.gross }}</p>

            
          <h2 class="text-lg font-semibold border-b pb-1 mt-4 mb-3">Deductions</h2>
          <p><strong>Basic Salary:</strong> INR {{ payroll.salary.basic }}</p>
          <p><strong>HRA:</strong> INR {{ payroll.salary.hra }}</p>
          <p><strong>Conveyance Allowance:</strong> INR {{ payroll.salary.conveyance }}</p>
          <p><strong>Other Allowances:</strong> INR {{ payroll.salary.allowances }}</p>
          <p class="font-bold mt-2"><strong>Gross Salary:</strong> INR {{ payroll.salary.gross }}</p>
  
          <h2 class="text-lg font-bold text-green-700 mt-4">Net Salary: INR {{ payroll.netSalary }}</h2>
        </div>
<div class="flex items-center justify-center mt-8 mb-8">
  <p class="text-center">This is sysstem genereted slip does not require any signature</p>
</div>
        
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: ["payroll"],
    data() {
      return {
        selectedYear: new Date().getFullYear(),
        selectedMonth: new Date().toLocaleString("default", { month: "long" }),
        years: [2023, 2024, 2025],
        months: ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"],
      };
    },
  };
  </script>
  