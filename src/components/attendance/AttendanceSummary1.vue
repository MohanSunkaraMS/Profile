<template>
    <div class="p-6 bg-gray-100 min-h-screen flex flex-col items-center">
        <div class="bg-white rounded-xl shadow-lg w-full max-w-6xl p-6">
            <!-- <div class="flex justify-between items-center mb-4">
          <h2 class="text-2xl  text-center font-semibold">22-28 February 2024</h2>
          <select class="border rounded p-2 text-gray-600">
            <option>Weekly</option>
          </select>
        </div> -->

            <div class="flex">
                <!-- Calendar Section -->
                <div class="w-1/4 bg-white p-4 rounded shadow-md">
                    <h3 class="font-semibold mb-2">February</h3>
                    <div class="grid grid-cols-7 gap-1 text-center text-sm">
                        <span v-for="day in days" :key="day" class="p-1">{{ day }}</span>
                    </div>
                    <div class="grid grid-cols-7 gap-1 mt-2 text-center">
                        <span v-for="(date, index) in dates" :key="index"
                            :class="['p-2 rounded-full', selectedDates.includes(date) ? 'bg-purple-300' : '']">
                            {{ date }}
                        </span>
                    </div>
                    <hr class="border-t-4 w-[107%] border-gray-300 my-4">



                    <div class="mt-4">
                        <h4 class="font-semibold">Legend</h4>
                        <ul>
                            <li class="flex items-center gap-2"><span class="w-4 h-4 bg-purple-400 rounded-full"></span>
                                Present</li>
                            <li class="flex items-center gap-2"><span class="w-4 h-4 bg-green-200 rounded-full"></span>
                                Paid Leave</li>
                            <li class="flex items-center gap-2"><span class="w-4 h-4 bg-yellow-200 rounded-full"></span>
                                Unpaid Leave</li>
                            <li class="flex items-center gap-2"><span class="w-4 h-4 bg-red-200 rounded-full"></span>
                                Week Off</li>
                            <li class="flex items-center gap-2"><span class="w-4 h-4 bg-blue-200 rounded-full"></span>
                                Holiday</li>
                        </ul>
                    </div>
                </div>
                <div class="border-l-4  border-gray-300 h-90"></div>

                <!-- Attendance Schedule Grid -->
                <div class="flex-1">
                    <div class="flex justify-between gap-4">

                        <div class="flex justify-between items-center mb-4">
                            <h4 class="text-2xl text-center mr-2 ml-4 font-semibold leading-[3rem]">
                                22-28 February 2024
                            </h4>


                            <select class="border rounded p-1 text-gray-600">
                                <option>Weekly</option>
                            </select>
                        </div>


                        <div class="flex items-center space-x-6">
                            <label class="flex items-center space-x-2">
                                <input type="checkbox" checked class="form-checkbox text-purple-600" />
                                <span>Attendance log</span>
                            </label>
                            <label class="flex items-center space-x-2">
                                <input type="checkbox" class="form-checkbox text-purple-600" />
                                <span>Leave log</span>
                            </label>
                        </div>


                    </div>
                    <hr class="border-t-4 w-[103%] border-gray-300 my-4">

                    <div class="flex mt-0">
                        <!-- Time Labels -->
                        <div class="w-16 border-r border-gray-300 text-right pr-2">
                            <div v-for="hour in hours" :key="hour"
                                class="h-16 flex items-center justify-end text-gray-600 text-sm">
                                {{ hour }}
                            </div>
                        </div>

                        <!-- Schedule Grid -->
                        <div class="flex-1 grid grid-cols-7 gap-0 border-t border-l border-gray-300">
                            <div v-for="day in week" :key="day" class="relative">
                                <!-- Day Heading (No Border) -->
                                <h4 class="text-center font-medium py-2 bg-gray-100">{{ day }}</h4>

                                <!-- Time Slots with Vertical Lines -->
                                <div v-for="hour in hours" :key="hour"
                                    class="h-12 border-b border-gray-300 border-r relative">
                                    <!-- Event Blocks -->
                                    <div v-if="(day === 'Monday' && hour === '09:00') || (day === 'Tuesday' && hour === '10:00')"
                                        class="w-6 bg-purple-400 h-8 absolute left-1/2 transform -translate-x-1/2">
                                    </div>
                                </div>

                                <!-- Highlighted Days -->
                                <div v-if="['Thursday', 'Friday', 'Saturday'].includes(day)"
                                    class="absolute inset-0 bg-purple-100 opacity-30 pointer-events-none">
                                </div>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            days: ['M', 'T', 'W', 'T', 'F', 'S', 'S'],
            dates: Array.from({ length: 28 }, (_, i) => i + 1),
            selectedDates: [22, 28],
            week: ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday'],
            hours: ['09:00', '10:00', '11:00', '12:00', '13:00', '14:00',]
        };
    }
};
</script>

<style scoped>
.form-checkbox {
    width: 1rem;
    height: 1rem;
}
</style>