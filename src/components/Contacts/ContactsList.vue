<template>
  <div
    class="max-w-lg mx-auto my-10 bg-white dark:bg-stone-800 p-8 rounded-xl shadow shadow-stone-300"
  >
    <div class="flex flex-row justify-between items-center">
      <div>
        <h1 class="text-3xl font-medium">Contacts list</h1>
      </div>
      <div class="inline-flex space-x-2 items-center">
        <button
          @click="showModal"
          class="p-2 border border-stone-200 rounded-md inline-flex space-x-1 items-center hover:bg-stone-200 dark:hover:bg-emerald-500 text-sm md:block"
        >
          Add Contact
        </button>
      </div>
    </div>
    <p class="text-stone-500">Hello, here are your latest contacts</p>

    <div id="tasks" class="my-5">
      <!-- Render contacts dynamically using v-for -->
      <div
        v-for="contact in contacts"
        :key="contact.id"
        class="flex justify-between items-center border-b border-stone-200 py-3 px-2 border-l-4 border-l-transparent"
      >
        <p class="text-stone-500">{{ contact.name }}</p>
        <p class="text-stone-500">{{ contact.number }}</p>
        <button>Delete</button>
      </div>
    </div>
    <p class="text-xs text-stone-500 text-center">Last updated 12 minutes ago</p>
  </div>
</template>

<script>
export default {
  props: {
    contacts: {
      type: Array,
      required: true
    }
  },
  methods: {
    showModal() {
      this.$emit('show-modal')
    }
  }
}
</script>
