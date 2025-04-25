<template>
  <div class="bg-white shadow-md h-fit w-full rounded-lg border">
    
    <!-- Header Section -->
    <div class="flex justify-between items-center bg-gray-100 px-4 py-3 rounded-t-lg border-b">
      <h2 class="text-lg text-[#898e90]">Contact</h2>
      <button class="text-blue-500 hover:underline">Edit</button>
    </div>

    <!-- Contact Details -->
    <div class="p-5 text-sm grid grid-cols-1 gap-y-3">
      <div class="flex">
        <span class="w-40 text-[#898e90]">Work Email:</span>
        <span>{{ contact.workEmail }}</span>
      </div>
      <div class="flex">
        <span class="w-40 text-[#898e90]">Work Number:</span>
        <span>{{ contact.workPhone }}</span>
      </div>

      <div class="flex">
        <span class="w-40 text-[#898e90]">Personal Email:</span>
        <span>{{ contact.personalEmail }}</span>
      </div>
      <div class="flex">
        <span class="w-40 text-[#898e90]">Personal Number:</span>
        <span>{{ contact.personalPhone }}</span>
      </div>
    </div>

    <!-- Emergency Contact 1 -->
    <div class="p-5 text-sm">
      <h3 class=" border-b pb-2">Emergency Contact 1</h3>
      <div class="grid grid-cols-1 gap-y-3 mt-3">
        <div class="flex">
          <span class="w-40 text-[#898e90]">Name:</span>
          <span>{{ contact.emergency1.name }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Relation:</span>
          <span>{{ contact.emergency1.relation }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Phone Number:</span>
          <span>{{ contact.emergency1.phone }}</span>
        </div>
      </div>
    </div>

    <!-- Emergency Contact 2 -->
    <div class="p-5 text-sm">
      <h3 class=" border-b pb-2">Emergency Contact 2</h3>
      <div class="grid grid-cols-1 gap-y-3 mt-3">
        <div class="flex">
          <span class="w-40 text-[#898e90]">Name:</span>
          <span>{{ contact.emergency2.name }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Relation:</span>
          <span>{{ contact.emergency2.relation }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Phone Number:</span>
          <span>{{ contact.emergency2.phone }}</span>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  props: ["contact"],
};
</script>
