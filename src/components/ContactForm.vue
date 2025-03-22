<script setup>
import { reactive } from 'vue'
import { Send } from 'lucide-vue-next'

const formState = reactive({
  name: '',
  email: '',
  message: '',
})

const handleSubmit = () => {
  console.log(formState)
  alert('Message sent! (This is a demo)')
}
</script>

<template>
  <div class="p-6 md:p-8" id="contact">
    <div class="mx-auto max-w-2xl">
      <h2
        class="mb-8 mt-20 inline-block rotate-1 border-4 border-black bg-white px-6 py-2 text-3xl font-black uppercase shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] md:text-4xl"
      >
        Get In Touch
      </h2>

      <form
        @submit.prevent="handleSubmit"
        class="rotate-1 transform border-4 border-black bg-orange-300 p-6 shadow-[8px_8px_0px_0px_rgba(0,0,0,1)] transition-all hover:shadow-[12px_12px_0px_0px_rgba(0,0,0,1)] md:p-8"
      >
        <div class="mb-6">
          <label class="mb-2 block font-black" for="name"> NAME </label>
          <input
            id="name"
            v-model="formState.name"
            required
            class="w-full -rotate-1 border-4 border-black bg-white p-6 text-lg shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] focus:outline-none"
          />
        </div>

        <div class="mb-6">
          <label class="mb-2 block font-black" for="email"> EMAIL </label>
          <input
            id="email"
            v-model="formState.email"
            type="email"
            required
            class="w-full rotate-1 border-4 border-black bg-white p-6 text-lg shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] focus:outline-none"
          />
        </div>

        <div class="mb-6">
          <label class="mb-2 block font-black" for="message"> MESSAGE </label>
          <textarea
            id="message"
            v-model="formState.message"
            required
            rows="5"
            class="w-full -rotate-1 border-4 border-black bg-white p-6 text-lg shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] focus:outline-none"
          ></textarea>
        </div>

        <button
          type="submit"
          class="flex w-full -rotate-2 items-center justify-center border-4 border-black bg-black px-8 py-6 text-lg font-black text-white shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] transition-all hover:rotate-0 hover:bg-gray-900 hover:shadow-[8px_8px_0px_0px_rgba(0,0,0,1)]"
        >
          <Send class="mr-2 h-5 w-5" />
          Send Message
        </button>
      </form>
    </div>
  </div>
</template>
