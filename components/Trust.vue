<template>
  <section class="bg-gray-100 py-16">
    <div class="max-w-4xl mx-auto px-4">
      <h2 class="text-4xl font-bold mb-8 text-center">Trusted by Many Companies</h2>
      <ul class="flex flex-wrap items-center justify-center flex-row">
        <li class="m-4">
          <img src="@/assets/img/sc.png" class="w-9 h-9" alt="" />
        </li>
        <li class="m-4">
          <img src="@/assets/img/crypto.png" class="w-9 h-9" alt="" />
        </li>
        <li class="m-4">
          <img src="@/assets/img/bk.png" class="w-9 h-9" alt="" />
        </li>
        <li class="m-4">
          <img src="@/assets/img/binance.png" class="w-9 h-9" alt="" />
        </li>
      </ul>
      <p class="mt-8 text-center text-gray-600 p-3">
        Join them and experience our top-notch services.
      </p>
      <a
        href="#contact"
        class="bg-gradient-to-tr from-[#0C0091] to-[#00A87E] text-white font-semibold py-3 px-4 rounded mt-8 justify-center items-center flex mx-auto md:max-w-md max-w-full"
        @click.prevent="handleClick('contact')"
      >
        Get Started
      </a>
    </div>
  </section>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      menuOpen: false,
    };
  },
  methods: {
    /* emit handleClick */
    handleClick(sectionId) {
      this.$emit("scrollToSection", sectionId);
    },
  },
};
</script>
