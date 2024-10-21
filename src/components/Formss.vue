<script setup>
import { EyeIcon } from "@heroicons/vue/solid";
</script>

<template>
  
  <div class="bg-white px-8 pt-11 w-80 mx-auto">
    <form>
      <div class="mb-4">
        <label class="block text-sm font-semibold mb-2">Username</label>
        <input
          type="text"
          class="w-full border border-gray-300 rounded-lg p-2"
        />
      </div>
      <div class="mb-1">
        <label class="block text-sm font-semibold mb-2">Password</label>
        <div class="relative">
          <input
            type="password"
            class="w-full border border-gray-300 rounded-lg p-2"
          />
          <EyeIcon
            class="absolute right-3 top-3 w-5 h-5 text-gray-500 cursor-pointer"
          />
        </div>
      </div>
      <div class="text-right mb-7">
        <span class="text-sm">Forgot </span>
        <a href="#" class="text-blue-500 text-sm underline"
          >username</a
        >
        <span class="text-sm"> or </span>
        <a href="#" class="text-blue-500 text-sm underline"
          >password?</a
        >
      </div>
      <button
        class="w-full bg-purple-700 text-white py-2 rounded-lg hover:bg-purple-800"
      >
        Sign in
      </button>
    </form>
    <div class="text-center mt-4">
      <a href="#" class="text-blue-500 text-sm">Create a new account</a>
    </div>
  </div>
</template>
