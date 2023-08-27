<template>
  <div>
    <nav
      class="text-gray-200 fixed top-0 left-0 right-0"
      :class="menuOpen ? 'bg-[#000] bg-opacity-70' : 'bg-transparent'"
    >
      <div
        class="flex items-center justify-between px-4 bg-[#000] bg-opacity-70"
        :class="menuOpen ? 'bg-transparent' : 'bg-[#000] bg-opacity-70'"
      >
        <a
          href="#home"
          @click.prevent="
            handleClick('home');
            menuOpen = false;
          "
          v-if="menuOpen"
        >
          <div class="flex items-center">
            <!-- Icon on the left -->

            <div class="mr-2">
              <img src="@/assets/img/bean-removebg-preview.png" class="h-20 w-20" />
            </div>
            <span class="font-semibold nav-hp">Beannsoft</span>
          </div>
        </a>
        <div class="hidden md:flex md:items-center md:space-x-4" v-if="menuOpen">
          <ul class="flex space-x-4 text-base">
            <!-- Menu items on the right -->
            <li>
              <a
                href="#how-we-work"
                @click.prevent="
                  handleClick('how-we-work');
                  
                "
                class="hover:text-gray-300"
                >How we work</a
              >
            </li>
            <li>
              <a
                href="#what-we-do"
                @click.prevent="
                  handleClick('what-we-do');
                  
                "
                class="hover:text-gray-300"
                >What we do</a
              >
            </li>
            <li>
              <a
                href="#pricing"
                @click.prevent="
                  handleClick('pricing');
                 
                "
                class="hover:text-gray-300"
                >Pricing</a
              >
            </li>
            <li>
              <a
                href="#contact"
                @click.prevent="
                  handleClick('contact');
                 
                "
                class="hover:text-gray-300"
                >Contact</a
              >
            </li>
            <li>
              <a
                href="#career"
                @click.prevent="
                  handleClick('career');
                
                "
                class="hover:text-gray-300"
                >Careers</a
              >
            </li>
            <li>
              <a
                href="#team"
                @click.prevent="
                  handleClick('team');
                  
                "
                class="hover:text-gray-300"
                >Team</a
              >
            </li>
          </ul>
        </div>
        <!-- Menu toggle button (for mobile) -->
        <div class="flex items-center py-3 bg-transparent">
          <button class="p-2 bg-transparent" @click="menuOpen = !menuOpen">
            <Icon
              :name="menuOpen ? 'ic:outline-cancel' : 'material-symbols:filter-list'"
              class="w-6 h-6 transition-transform duration-300 transform"
            />
          </button>
        </div>
      </div>
    </nav>

    <!-- Responsive menu (for mobile) -->
    <div
      class="md:hidden mt-14 pb-2 fixed w-full bg-[#000] bg-opacity-70"
      :class="menuOpen ? 'block' : 'hidden'"
      v-show="menuOpen"
    >
      <ul
        class="text-gray-200 px-4 py-2 gap-y-5 flex justify-start items-start flex-col bg-[#000] bg-opacity-70"
        :class="menuOpen ? 'bg-transparent' : 'bg-[#000] bg-opacity-70'"
      >
        <li>
          <a
            href="#how-we-work"
            @click.prevent="
              handleClick('how-we-work');
             
            "
            class="block"
            >How we work</a
          >
        </li>
        <li>
          <a
            href="#what-we-do"
            @click.prevent="
              handleClick('what-we-do');
            
            "
            class="block"
            >What we do</a
          >
        </li>
        <li>
          <a
            href="#pricing"
            @click.prevent="
              handleClick('pricing');
              
            "
            class="block"
            >Pricing</a
          >
        </li>
        <li>
          <a
            href="#contact"
            @click.prevent="
              handleClick('contact');
              
            "
            class="block"
            >Contact</a
          >
        </li>
        <li>
          <a
            href="#career"
            @click.prevent="
              handleClick('career');
              
            "
            class="block"
            >Careers</a
          >
        </li>
        <li>
          <a
            href="#team"
            @click.prevent="
              handleClick('team');
              
            "
            class="block"
            >Team</a
          >
        </li>
      </ul>
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
  methods: {
    /* emit handleClick */
    handleClick(sectionId) {
      this.$emit("scrollToSection", sectionId);
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Acme&display=swap");
.nav-hp {
  font-family: "Acme", sans-serif;
  font-size: 1.5rem;
}
</style>
