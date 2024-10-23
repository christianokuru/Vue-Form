<script setup></script>


<template>
  <div :class="['lg:flex-row lg:items-center mt-8 mx-5']">
    <!-- Footer container -->
    <footer :class="['flex flex-col items-center text-center text-[#5b2f91] font-semibold text-xs border-t border-dotted pt-4 border-gray-700 lg:flex-row md:space-x-3 lg:items-center lg:py-6 lg:container lg:mx-auto lg:justify-center']">
      
      <!-- Copyright for large screens -->
      <div :class="['hidden md:block text-left text-gray-700 lg:w-1/5 font-extralight lg:flex-row lg:space-x-3 items-center lg:pb-3 text-xs']">
        <p :class="['mt-2 lg:whitespace-nowrap']">© 2002-2024 Teladoc, Inc. All rights reserved.</p>
      </div>

      <!-- Purple Links -->
      <div :class="[' flex flex-col items-center space-y-2 lg:flex-row lg:space-y-0 lg:space-x-6 lg:w-2/3 lg:justify-end px-1']">
        <router-link to="#">
          <p :class="['hover:text-[#a77bca] text-[#5b2f91] pb-1 whitespace-nowrap']">Terms of Service</p>
        </router-link>
        <router-link to="#">
          <p :class="['hover:text-[#a77bca] text-[#5b2f91] pb-1 whitespace-nowrap']">Notice of Privacy Practices</p>
        </router-link>
        <router-link to="#">
          <p :class="['hover:text-[#a77bca] text-[#5b2f91] pb-1 break-words lg:whitespace-nowrap']">
            Notice of Non-Discrimination and Language Assistance
          </p>
        </router-link>
        <router-link to="#">
          <p :class="['hover:text-[#a77bca] text-[#5b2f91] pb-1 whitespace-nowrap']">Informed Consent Agreement</p>
        </router-link>
      </div>

      <!-- Copyright for small screens -->
      <div :class="['text-center text-gray-700 lg:hidden mt-4 font-thin']">
        <p :class="['mt-2 mb-28']">© 2002-2024 Teladoc, Inc. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

