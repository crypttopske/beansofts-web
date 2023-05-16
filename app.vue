<template>
  <div class="">
    <div class="py-4 bg-img">
      <div class="">
        <Navi />
      </div>
      <Hero />
    </div>
    <Trust />
    <WhatWeDo />
    <div class="bg-work py-3 pt-5">
      <HowWeDo />
      <Pricing />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      menuOpen: false,
    };
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
