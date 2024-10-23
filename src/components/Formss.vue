<script setup>
import { EyeIcon } from "@heroicons/vue/solid";
</script>

<template>
  
  <div class="bg-white px-12 pt-9 w-80 mx-auto md:w-1/3 md:mb-24">
    <h1 class="hidden md:block md:text-4xl md:font-bold md:mb-10 ">Sign in to your account</h1>
    <form>
      <!-- Username field -->
      <div class="mb-4">
        <label class="block text-sm font-semibold mb-2">Username</label>
        <input
          type="text"
          class="w-full border border-gray-500 rounded-lg p-2"
        />
      </div>
      <!-- Password field -->
      <div class="mb-0 mt-[-7px]">
        <label class="block text-sm font-semibold mb-2">Password</label>
        <div class="relative">
          <input
            type="password"
            class="w-full border border-gray-500 rounded-lg p-2"
          />
          <EyeIcon
            class="absolute right-3 top-3 w-5 h-5 text-gray-500 cursor-pointer"
          />
        </div>
      </div>
      <!-- Sign in Button -->
      <div class="text-right mb-6">
        <span class="text-xs">Forgot </span>
        <a href="#" class="text-[#0060fc] text-xs underline font-semibold"
          >username</a
        >
        <span class="text-xs"> or </span>
        <a href="#" class="text-[#0060fc] text-xs underline font-semibold"
          >password?</a
        >
      </div>
      <button
        class="w-full bg-[#5b2f91] text-white py-2 font-semibold rounded-lg hover:bg-purple-800"
      >
        Sign in
      </button>
    </form>
    <div class="text-center mt-4">
      <a href="#" class="text-[#0060fc] text-sm font-semibold">Create a new account</a>
    </div>
  </div>
</template>
