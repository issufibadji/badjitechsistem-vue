<template>
  <div class="min-h-screen bg-blue-50 text-gray-900 flex justify-center">
    <div class="max-w-screen-xl m-0 sm:m-10 bg-white shadow sm:rounded-lg flex justify-center flex-1">
      <div class="lg:w-1/2 xl:w-5/12 p-6 sm:p-12">
        <div>
          <img src="/src/assets/images/logo-azul-sem-fundo.png" class="w-36 mx-auto" />
        </div>
        <div class="mt-8 flex flex-col items-center">
          <h1 class="text-2xl xl:text-3xl font-extrabold text-blue-800">Sign up</h1>

          <div class="w-full flex-1 mt-8">
            <div class="flex flex-col items-center">
              <button
                class="w-full max-w-xs font-bold shadow-sm rounded-lg py-3 bg-blue-100 text-blue-900 flex items-center justify-center hover:bg-blue-200">
                <div class="bg-white p-1 rounded-full">
                  <img src="/src/assets/images/logo-branco-azul.png" class="w-5 h-5 rounded-full" />
                </div>
                <span class="ml-4">Sign Up with BadjiTech</span>
              </button>

              <button
                class="w-full max-w-xs font-bold shadow-sm rounded-lg py-3 bg-blue-100 text-blue-900 flex items-center justify-center hover:bg-blue-200 mt-5">
                <div class="bg-white p-2 rounded-full">
                  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" class="w-4 h-4" />
                </div>
                <span class="ml-4">Sign Up with GitHub</span>
              </button>
            </div>

            <div class="my-12 border-b text-center">
              <div class="leading-none px-2 inline-block text-sm text-blue-600 font-medium bg-white">Or sign up with e-mail</div>
            </div>

            <div class="mx-auto max-w-xs">
              <input type="email" placeholder="Email"
                class="w-full px-8 py-4 rounded-lg bg-blue-50 border border-blue-200 placeholder-blue-600 text-sm focus:outline-none focus:border-blue-400 focus:bg-white" />
              <input type="password" placeholder="Password"
                class="w-full px-8 py-4 rounded-lg bg-blue-50 border border-blue-200 placeholder-blue-600 text-sm focus:outline-none focus:border-blue-400 focus:bg-white mt-5" />
              <button
                class="mt-5 w-full py-4 rounded-lg bg-blue-700 text-white font-semibold hover:bg-blue-800 flex items-center justify-center">
                <svg class="w-6 h-6 -ml-2" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <path d="M16 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2" />
                  <circle cx="8.5" cy="7" r="4" />
                  <path d="M20 8v6M23 11h-6" />
                </svg>
                <span class="ml-3">Sign Up</span>
              </button>
              <p class="mt-6 text-xs text-blue-600 text-center">
                I agree to abide by templatana's <a href="#" class="border-b border-blue-500">Terms of Service</a> and <a href="#" class="border-b border-blue-500">Privacy Policy</a>
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="flex-1 bg-blue-100 text-center hidden lg:flex">
        <div class="m-12 xl:m-16 w-full bg-contain bg-center bg-no-repeat"
          style="background-image: url('https://storage.googleapis.com/devitary-image-host.appspot.com/15848031292911696601-undraw_designer_life_w96d.svg');">
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
</style>