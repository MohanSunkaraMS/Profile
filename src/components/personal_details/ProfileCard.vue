<template>
  <div class="bg-gray-100 w-full shadow-md rounded-lg p-8 mb-6 mx-auto flex items-center space-x-6">
    <!-- Profile Image -->
    <img :src="user.image" alt="Profile Picture" class="w-36 h-36 rounded-lg object-cover" />

    <!-- User Details -->
    <div class="flex-1">
      <h2 class="text-xl font-semibold text-gray-900">{{ user.name }}</h2>

      <!-- User Info (ID, Role, Email, Phone, Location) -->
      <div class="text-gray-600 flex flex-wrap items-center space-x-4 mt-2">
        <span class="flex items-center">
          <i class="fas fa-id-badge mr-1 text-gray-500"></i> {{ user.id }}
        </span>
        <span class="flex items-center">
          <i class="fas fa-briefcase mr-1 text-gray-500"></i> {{ user.role }}
        </span>
        <span class="flex items-center">
          <i class="fas fa-envelope mr-1 text-gray-500"></i> {{ user.email }}
        </span>
        <span class="flex items-center">
          <i class="fas fa-phone mr-1 text-gray-500"></i> {{ user.phone }}
        </span>
        <span class="flex items-center">
          <i class="fas fa-map-marker-alt mr-1 text-gray-500"></i> {{ user.location }}
        </span>
      </div>
   
      <hr class="border-gray-300 my-4">




      <!-- Department & Reporting Manager -->
      <div class="mt-1 text-gray-600 flex items-center space-x-8">
        <span>
          <span class="font-semibold mr-1">Department:</span>
          <span class="text-blue-600 font-medium">{{ user.department }}</span>
        </span>
        <span>
          <span class="font-semibold mr-1">Reporting Manager:</span>
          <span class="text-blue-600 font-medium ">
            <i class="fas fa-user-tie mr-1"></i> {{ user.manager }}
          </span>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    user: Object, // This component expects a user object as a prop
  },
};
</script>

<style scoped>
/* You can add more styles here if needed */
</style>
