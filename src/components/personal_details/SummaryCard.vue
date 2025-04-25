<template>
  <div class="bg-white shadow-md h-fit w-[100%] rounded-lg border">

    <!-- <div class="flex justify-between items-center bg-gray-100 px-4 py-3 rounded-t-lg border-b">
        <h2 class="text-lg font-semibold">Summary</h2>
        <button class="text-blue-500 hover:underline">Edit</button>
      </div> -->
    <div class="text-sm">
      <div class="border bg-gray-100  rounded-lg shadow-sm  bg-white">
        <div class="flex justify-between  bg-gray-100 items-center border-b p-2 mb-4">
          <h2 class="font-semibold text-lg">Summary</h2>
          <a href="#" class="text-blue-500 text-sm">Edit</a>
        </div>
        <div class="grid grid-cols-2 gap-y-3 p-5 text-sm">
  <div class="flex">
    <span class="w-40 text-[#898e90]">First Name:</span> <span>Devashish</span>
  </div>
  <div class="flex">
    <span class="w-40 text-[#898e90]">Middle Name:</span> <span>-</span>
  </div>

  <div class="flex">
    <span class="w-40 text-[#898e90]">Last Name:</span> <span>Bariko</span>
  </div>
  <div class="flex">
    <span class="w-40 text-[#898e90]">Gender:</span> <span>Male</span>
  </div>

  <div class="flex">
    <span class="w-40 text-[#898e90]">Display Name:</span> <span>Dev Bariko</span>
  </div>
  <div class="flex">
    <span class="w-40 text-[#898e90]">DOB:</span> <span>06-10-1998</span>
  </div>

  <div class="flex">
    <span class="w-40 text-[#898e90]">Marital Status:</span> <span>Single</span>
  </div>
  <div class="flex">
    <span class="w-40 text-[#898e90]">Blood Group:</span> <span>B+ve</span>
  </div>

  <div class="flex">
    <span class="w-40 text-[#898e90]">Nationality:</span> <span>India</span>
  </div>
  <div class="flex">
    <span class="w-40 text-[#898e90]">Handicapped:</span> <span>-</span>
  </div>
</div>


      </div>

    </div>


  </div>
</template>

<script>
export default {
  props: ["summary"],
};
</script>