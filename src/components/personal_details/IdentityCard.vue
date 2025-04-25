<template>
  <div class="bg-white shadow-md h-fit w-full rounded-lg border">
    
    <!-- Header Section -->
    <div class="flex justify-between items-center bg-gray-100 px-4 py-3 rounded-t-lg border-b">
      <h2 class="text-lg">Identity</h2>
    </div>

    <!-- Photo Identification Section -->
    <div class="p-5 text-sm border-b">
      <div class="flex justify-between">
        <h3 class="font-semibold">Photo Identification</h3>
        <a href="#" class="text-blue-500 hover:underline text-sm">Add details</a>
      </div>
      
      <div class="grid grid-cols-1 gap-y-3 mt-3">
        <div class="flex">
          <span class="w-40 text-[#898e90]">Unique ID number:</span>
          <span>123456789</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Name:</span>
          <span>KOti</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Date of Birth:</span>
          <span>{{ identity.dob }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Parent's Name:</span>
          <span>Priyaknara</span>
        </div>
      </div>
    </div>

    <!-- Address Proof Section -->
    <div class="p-5 text-sm">
      <div class="flex justify-between">
        <h3 class="font-semibold">Address Proof</h3>
        <a href="#" class="text-blue-500 hover:underline text-sm">Add details</a>
      </div>

      <div class="grid grid-cols-1 gap-y-3 mt-3">
        <div class="flex">
          <span class="w-40 text-[#898e90]">Unique ID number:</span>
          <span>{{ identity.uniqueId }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Name:</span>
          <span>{{ identity.name }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Date of Birth:</span>
          <span>{{ identity.dob }}</span>
        </div>
        <div class="flex">
          <span class="w-40 text-[#898e90]">Parent's Name:</span>
          <span>{{ identity.parentName }}</span>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  props: ["identity"],
};
</script>
