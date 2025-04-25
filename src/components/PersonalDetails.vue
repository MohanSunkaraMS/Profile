<template>
  <div class="container mx-auto">
    <!-- Profile Card -->
    <ProfileCard :user="user" />

    <!-- Summary & Contact Section -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-4">
      <div class="flex flex-col gap-4">
        <SummaryCard :summary="summary" />
        <AddressCard :address="address" />
      </div>
      <ContactCard :contact="contact" />
    </div>

    <!-- Identity & Job Details Section -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-4">
      <IdentityCard :identity="summary" />
      <OtherDetailsCard :jobDetails="jobDetails" :organization="organization" :policies="policies" />
    </div>
  </div>
</template>

<script>
import ProfileCard from "./personal_details/ProfileCard.vue";
import SummaryCard from "./personal_details/SummaryCard.vue";
import ContactCard from "./personal_details/ContactCard.vue";
import AddressCard from "./personal_details/AddressCard.vue";
import IdentityCard from "./personal_details/IdentityCard.vue";
import OtherDetailsCard from "./personal_details/OtherDetailsCard.vue";

export default {
  components: {
    ProfileCard,
    SummaryCard,
    ContactCard,
    AddressCard,
    IdentityCard,
    OtherDetailsCard,
  },
  data() {
    return {
      user: {
        name: "John Doe",
        id: "EMP12345",
        role: "Software Engineer",
        email: "john.doe@example.com",
        phone: "+1234567890",
        location: "New York, USA",
        image: "https://images.ctfassets.net/h6goo9gw1hh6/2sNZtFAWOdP1lmQ33VwRN3/24e953b920a9cd0ff2e1d587742a2472/1-intro-photo-final.jpg?w=1200&h=992&fl=progressive&q=70&fm=jpg",
        manager: "Vineel Reddy",
        department: "Operations",
      },
      summary: {
        firstName: "John",
        middleName: "A.",
        lastName: "Doe",
        gender: "Male",
        displayName: "John Doe",
        dob: "1990-01-01",
        maritalStatus: "Single",
        bloodGroup: "O+",
        nationality: "American",
        handicapped: "No",
      },
      contact: {
        workEmail: "john.doe@company.com",
        workPhone: "+1234567890",
        personalEmail: "john.doe@gmail.com",
        personalPhone: "+0987654321",
        emergency1: { name: "Jane Doe", relation: "Sister", phone: "+1122334455" },
        emergency2: { name: "Sam Doe", relation: "Friend", phone: "+6677889900" },
      },
      address: {
        current: "123, New York City, USA",
        permanent: "456, California, USA",
      },
      jobDetails: {
        employeeId: "ASK 083",
        dateOfJoining: "3 Jun, 2024",
        jobTitle: "Product Manager",
        workType: "Full-time",
        inProbation: "-",
        noticePeriod: "60 days",
        contractStatus: "N/A",
        shift: "General",
      },
      organization: {
        company: "Asakta Electronics and Communication Pvt Ltd",
        department: "Information Technology",
        reportingManager: "Vineel Reddy",
        l2Manager: "-",
      },
      policies: {
        weeklyOffPolicy: "-",
        attendanceCapture: "General Capture Scheme",
        attendancePenalization: "Aquaponics",
        leavePolicy: "General Leave Policy",
        travelPolicy: "-Not Set-",
        loanPolicy: "-Not Set-",
      },
    };
  },
};
</script>
