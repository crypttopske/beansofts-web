<template>
  <div class="">
    <div class="py-4 bg-img">
      <div class="">
        <Navi @scrollToSection="scrollToSection" />
      </div>
      <Hero />
    </div>
    <Trust />

    <div class="mt-8">
      <WhatWeDo id="what-we-do" />
    </div>
    <div class="mt-8">
      <div class="bg-work py-3 pt-5">
        <HowWeDo id="how-we-work" />
        <Pricing id="pricing" />
      </div>
    </div>
    <div class="mt-8">
      <Team id="team" />
    </div>
    <div class="mt-8">
      <Contact id="contact" />
    </div>
    <div class="mt-8">
      <Career id="career" />
    </div>

    <About />

    <EndFooter />
  </div>
</template>
<script>
export default {
  data() {
    return {
      menuOpen: false,
    };
  },
  methods: {
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: "smooth" });
      }
    },
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");
.bg-img {
  background-image: linear-gradient(134deg, #0c0091 0%, #00a87e 100%);
}
.bg-work {
  background: #0a007e;
  background-size: cover;
}
* {
  font-family: "Poppins", sans-serif;
}
.transition-transform {
  transition-property: transform;
}
.transform {
  transform-origin: center;
}
.transform-rotate-180 {
  transform: rotate(180deg);
}
</style>
