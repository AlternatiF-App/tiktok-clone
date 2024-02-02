<template>
  <div class="text-center text-[28px] mb-4 font-bold">Sign Up</div>
  
  <div class="px-6 pb-2">
    <TextInput 
    placeholder="Fullname"
    v-model:input="name"
    inputType="text"
    :autoFocus="true"
    :error="errors && errors.name ? errors.name[0] : ''"
    />
  </div>

  <div class="px-6 pb-2">
    <TextInput 
    placeholder="Email address"
    v-model:input="email"
    inputType="email"
    :autoFocus="true"
    :error="errors && errors.email ? errors.email[0] : ''"
    />
  </div>

  <div class="px-6 pb-2">
    <TextInput 
      placeholder="Password"
      v-model:input="password"
      inputType="password"
    />
  </div>

  <div class="px-6 pb-2">
    <TextInput 
      placeholder="Confirm Password"
      v-model:input="confirmPassword"
      inputType="password"
    />
  </div>

  <div class="px-6 text-[12px] text-gray-600">Forgot password?</div>

  <div class="px-6 pb-2 mt-6">
    <button 
      :disabled="(!fullname || !email || !password || !confirmPassword)"
      :class="(!fullname || !email || !password || !confirmPassword) ? 'bg-gray-200' : 'bg-[#F02C56]'"
      @click="register()" 
      class="w-full text-[17px] font-semibold text-white py-3 rounded-sm"
    >
      Sign Up
    </button>
  </div>
</template>

<script setup>
let name = ref(null)
let email = ref(null)
let password = ref(null)
let confirmPassword = ref(null)
let errors = ref(null)
</script>