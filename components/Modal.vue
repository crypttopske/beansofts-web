<template>
  <div v-if="isOpen">
    <div
      class="fixed inset-0 bg-gray-800 bg-opacity-50 flex justify-center items-center z-50 overflow-auto"
    >
      <div
        class="bg-white sm:w-3/4 p-6 w-full rounded-lg shadow-lg transform transition-all duration-1000 ease-in-out sm:overflow-auto sm:mt-20 max-h-screen"
        style="overflow-y: auto"
      >
        <div class="mb-4"></div>
        <div class="mb-4">
          <h2 class="text-xl text-gray-800">{{ card }}</h2>
        </div>

        <div class="flex justify-end">
          <button
            @click="closeModal"
            class="bg-gradient-to-tr from-[#0C0091] to-[#00A87E] text-white font-semibold py-2 px-4 rounded mt-8 justify-center items-center flex mx-auto"
          >
            Close
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    isOpen: {
      type: Boolean,
      default: false,
    },
    card: {
      type: String,
      default: "",
    },
  },
  data() {
    return {};
  },
  methods: {
    closeModal() {
      this.$emit("close");
    },
  },
};
</script>

<style lang="scss" scoped></style>
