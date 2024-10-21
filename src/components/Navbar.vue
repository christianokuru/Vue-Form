<script setup>
import { ref } from 'vue'
import { LocationMarkerIcon, GlobeIcon} from '@heroicons/vue/solid'

// Dropdown options
const locations = ['USA', 'International', 'Canada', 'Denmark', 'Other Country']
const languages = ['Englsih', 'Spanish']

// State for the dropdown options
const dropdownOpen = ref(null)
const selectedLocation = ref('USA')
const selectedLanguage = ref('ENG')

// Functions
const toggleDropdown = (type) => {
  dropdownOpen.value = dropdownOpen.value === type ? null : type
}

const selectLocation = (location) => {
  selectedLocation.value = location
  dropdownOpen.value = null
}

const selectLanguage = (language) => {
  selectedLanguage.value = language
  dropdownOpen.value = null
}
</script>


<template>
    <div class="flex flex-col items-center justify-between mx-6 pt-9 border-b pb-1 border-gray-300">
      <!-- Navbar -->
      <header class="w-full bg-white p-4 flex justify-between items-center">
        <div class="flex items-center space-x-2">
          <img src="https://s3.amazonaws.com/images.teladoc.com/member/Logo-Horz-RGB.svg" alt="Teladoc Logo" class="w-28" />
        </div>

        <!--Location Dropdown 1 -->
        <div class="flex space-x-2 items-center">
          <div class="relative" @click="toggleDropdown('location')">
            <div class="flex items-center cursor-pointer space-x-1">
              <LocationMarkerIcon class="w-8 h-8 text-gray-700 border rounded-full p-2 shadow-sm" />
              <span>{{ selectedLocation }}</span>
            </div>
            <div v-if="dropdownOpen === 'location'" class="absolute right-0 mt-2 w-36 bg-white border border-gray-300 rounded-lg shadow-xl">
              <ul>
                <li v-for="location in locations" :key="location" @click="selectLocation(location)" class="p-2 px-4 hover:bg-gray-200 cursor-pointer border-b border-gray-300">{{ location }}</li>
              </ul>
            </div>
          </div>
  
          <!--Language Dropdown 2 -->
          <div class="relative" @click="toggleDropdown('language')">
            <div class="flex items-center cursor-pointer space-x-1">
              <GlobeIcon class="w-8 h-8 text-gray-700 border rounded-full p-2 shadow-sm" />
              <span>{{ selectedLanguage }}</span>
            </div>
            <div v-if="dropdownOpen === 'language'" class="absolute right-0 mt-2 w-24 bg-white border border-gray-300 rounded-lg shadow-lg">
              <ul>
                <li v-for="language in languages" :key="language" @click="selectLanguage(language)" class="p-2 hover:bg-gray-200 cursor-pointer border-b border-gray-300">{{ language }}</li>
              </ul>
            </div>
          </div>
        </div>
      </header>
      </div>
</template>
