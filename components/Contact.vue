<template>
  <div class="bg-gray-100 py-8 px-4 sm:px-6 lg:px-8">
    <div class="max-w-6xl mx-auto">
      <div class="flex justify-center items-center font-bold pt-2 pb-2">
        <h3 class="text-md text-gray-500 font-light pb-1 border-b border-gray-200">
          Contact Us
        </h3>
      </div>

      <div class="max-w-md mx-auto bg-white rounded-lg shadow-md overflow-hidden">
        <form class="px-6 py-4" @submit.prevent="submitForm">
          <div class="mb-4">
            <label for="name" class="block font-medium text-gray-700">Name</label>
            <input
              type="text"
              id="name"
              v-model="form.name"
              class="form-input mt-1"
              required
            />
          </div>

          <div class="mb-4">
            <label for="email" class="block font-medium text-gray-700">Email</label>
            <input
              type="email"
              id="email"
              v-model="form.email"
              class="form-input mt-1"
              required
            />
          </div>

          <div class="mb-4">
            <label for="message" class="block font-medium text-gray-700">Message</label>
            <textarea
              id="message"
              v-model="form.message"
              class="form-textarea mt-1"
              rows="4"
              required
            ></textarea>
          </div>

          <div class="flex justify-center">
            <button
              type="submit"
              class="bg-gradient-to-tr from-[#0C0091] to-[#00A87E] text-white font-medium py-2 px-4 rounded focus:outline-none"
            >
              Send Message
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: "",
        email: "",
        message: "",
      },
    };
  },
  methods: {
    submitForm() {
      // Perform form submission logic here
      console.log("Form submitted!", this.form);

      // Reset the form fields
      this.form.name = "";
      this.form.email = "";
      this.form.message = "";
    },
  },
};
</script>

<style scoped>
.form-input,
.form-textarea {
  appearance: none;
  background-color: #edf2f7;
  border-color: #e2e8f0;
  border-radius: 0.375rem;
  padding: 0.75rem 1rem;
  width: 100%;
}

.form-textarea {
  resize: vertical;
}
</style>
