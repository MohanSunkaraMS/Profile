<template>
  <div class="bg-white shadow-md h-fit w-[100%] rounded-lg border">
    <div class="flex justify-between items-center bg-gray-100 px-4 py-3 rounded-t-lg border-b">
      <h2 class="text-lg font-semibold">Address</h2>
      <button class="text-blue-500 hover:underline">Edit</button>
    </div>
    <div class="p-4 text-sm">
      <p><span class="text-[#898e90]">Current:</span> Sai Residency, Flat No. 204, Road No. 12, Banjara Hills, Hyderabad, Telangana - 500034</p>
      <p class="mt-2"><span class="text-[#898e90]">Permanent:</span> Flat No. 102, VR Classic, Simon Nagar, Kurmannapalem, Visakhapatnam, Andhra Pradesh, India - 530046</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["address"],
};
</script>
