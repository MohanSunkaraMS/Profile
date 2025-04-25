<template>
  <div class="container mx-auto p-4">
    <PayrollSummary :payroll="payroll" />
    <!-- <StatutoryInformation /> ✅ Added Statutory Information Component -->
    <div class="flex gap-x-0 mt-5">
      <Payslips :payroll="payroll" />
      <div class="flex flex-col">
        <Summary />
        <StatutoryInformation />  <!-- Fixed casing issue -->
      </div>
    </div>
  </div>
</template>

<script>
import { reactive } from "vue";
import PayrollSummary from "./mypayroll/PayrollSummary.vue";
import Payslips from "./mypayroll/Payslips.vue";
import Summary from "./mypayroll/Summary.vue";
import StatutoryInformation from"./mypayroll/statutoryInformation.vue"; // ✅ Fixed casing

export default {
  components: { PayrollSummary, Payslips, Summary, StatutoryInformation },
  setup() {
    const payroll = reactive({
      cycle: "Monthly",
      processCycle: "February 2025",
      compensation: "INR 930000",
      workingDays: "21",
      lastCycle: "January 2025",
      lossOfPay: "2",
      employee: {
        name: "John Doe",
        id: "IND12345",
        designation: "Consultant",
        department: "IT Services",
        doj: "01-Aug-2023",
        location: "Hyderabad",
      },
      salary: {
        basic: "80,000",
        hra: "20,000",
        conveyance: "5,000",
        allowances: "10,000",
        gross: "1,15,000",
      },
      netSalary: "98,800",
    });

    return { payroll };
  },
};
</script>

<style scoped>
/* Add custom styles here if needed */
</style>
