<template>
    <div class="w-[150%] bg-white shadow-md rounded-lg border h-fit inline-block">
        <div class="flex justify-between items-center bg-gray-100 px-4 py-3 rounded-t-lg border-b">
            <h2 class="text-lg font-semibold">Payment Information</h2>
        </div>
        <div class="p-4 grid grid-cols-1 gap-y-2">
            <p><span class="text-gray-500">Bank:</span> <span class="font-semibold">State Bank of India (SBI)</span></p>
            <p><span class="text-gray-500">Account No.:</span> <span class="font-semibold">302485761234</span></p>
            <p><span class="text-gray-500">IFSC Code:</span> <span class="font-semibold">SBIN0004567</span></p>
            <p><span class="text-gray-500">Name on Acc.:</span> <span class="font-semibold">Devashish Bariko</span></p>
        </div>
    </div>
</template>
<script setup>
const keys = ["id", "name", "email"];
const values = [
  [1, "Alice", "alice@example.com"],
  [2, "Bob", "bob@example.com"],
  [3, "Charlie", "charlie@example.com"]
];



</script>