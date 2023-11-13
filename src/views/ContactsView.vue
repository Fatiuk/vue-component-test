<template>
  <div class="min-h-screen py-6 flex flex-col justify-center sm:py-12">
    <div class="relative py-3 sm:max-w-xl sm:mx-auto">
      <div
        class="absolute inset-0 bg-gradient-to-r from-green-300 to-emerald-600 shadow-lg transform -skew-y-6 sm:skew-y-0 sm:-rotate-6 sm:rounded-3xl"
      ></div>
      <div class="relative px-4 py-10 bg-white dark:bg-stone-800 shadow-lg sm:rounded-3xl sm:p-20">
        <div class="max-w-md mx-auto">
          <div>
            <h1 class="text-2xl font-semibold">Login Form with Floating Labels</h1>
          </div>
          <div class="divide-y divide-stone-200 dark:text-stone-400">
            <div class="py-8 text-base leading-6 space-y-8 sm:text-lg sm:leading-7">
              <div class="relative">
                <input
                  autocomplete="off"
                  id="name"
                  name="name"
                  class="peer bg-transparent placeholder-transparent h-10 w-full border-b-2 border-stone-300 focus:outline-none focus:borer-rose-600"
                  placeholder="Contact name"
                />
                <label
                  for="name"
                  class="absolute left-0 -top-3.5 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-stone-440 peer-placeholder-shown:top-2 transition-all peer-focus:-top-3.5 peer-focus:text-stone-600 peer-focus:text-sm"
                  >Contact name</label
                >
              </div>
              <div class="relative">
                <input
                  autocomplete="off"
                  id="number"
                  name="number"
                  class="peer bg-transparent placeholder-transparent h-10 w-full border-b-2 border-stone-300 text-stone-900 focus:outline-none focus:borer-rose-600"
                  placeholder="Phone number"
                />
                <label
                  for="number"
                  class="absolute left-0 -top-3.5 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-stone-440 peer-placeholder-shown:top-2 transition-all peer-focus:-top-3.5 peer-focus:text-stone-600 peer-focus:text-sm"
                  >Phone number</label
                >
              </div>
              <div class="relative flex justify-center">
                <button class="bg-emerald-500 text-white rounded-md px-4 py-2 content-center">
                  Add Contact
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>
