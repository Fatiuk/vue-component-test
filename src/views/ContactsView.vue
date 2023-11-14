<template>
  <main>
    <ContactsForm
      v-if="modalVisible"
      @show-modal="showModal"
      @close="closeModal"
      @add-contact="addContact"
    />
    <ContactsList
      v-else
      :contacts="contacts"
      @show-modal="showModal"
      @delete-contact="deleteContact"
    />
  </main>
</template>

<script>
import ContactsForm from '../components/Contacts/ContactsForm.vue'
import ContactsList from '../components/Contacts/ContactsList.vue'

export default {
  components: {
    ContactsForm,
    ContactsList
  },

  data() {
    return {
      contacts: [
        { id: 'id-1', name: 'Rosie Simpson', number: '459-12-56' },
        { id: 'id-2', name: 'Hermione Kline', number: '443-89-12' },
        { id: 'id-3', name: 'Eden Clements', number: '645-17-79' },
        { id: 'id-4', name: 'Annie Copeland', number: '227-91-26' }
      ],
      modalVisible: false
    }
  },

  mounted() {
    const savedContacts = localStorage.getItem('contacts')
    if (savedContacts) {
      this.contacts = JSON.parse(savedContacts)
    } else {
      this.saveContactsToLocal()
    }
  },

  methods: {
    showModal() {
      this.modalVisible = true
    },

    closeModal() {
      this.modalVisible = false
    },

    addContact(contact) {
      this.contacts.push(contact)
      this.saveContactsToLocal()
    },

    deleteContact(id) {
      const index = this.contacts.findIndex((contact) => contact.id === id)
      if (index !== -1) {
        this.contacts.splice(index, 1)
      }
      this.saveContactsToLocal()
    },

    saveContactsToLocal() {
      localStorage.setItem('contacts', JSON.stringify(this.contacts))
    }
  }
}
</script>
