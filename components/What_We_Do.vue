<template>
  <div class="container mx-auto">
    <!-- what we do -->
    <div class="text-center">
      <div class="flex justify-center items-center font-bold pt-2 pb-2">
        <h3 class="text-md text-gray-500 font-light pb-1 border-b border-gray-200">
          What we do
        </h3>
      </div>
      <p class="text-gray-600">
        We provide a wide range of software development services to help you achieve your
        business goals.
      </p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-4">
      <div v-for="(card, index) in cards" :key="index" class="bg-white p-4 shadow">
        <img
          :src="card.image"
          alt="Card Image"
          class="md:w-20 w-16 rounded-full h-auto object-cover mb-4"
        />
        <div class="text-lg font-semibold mb-2">{{ card.title }}</div>
        <p class="text-gray-500 mb-4">{{ card.description.slice(0, 30) + ".." }}</p>
        <button class="text-blue-500 hover:underline" @click="isOpen = true">
          Learn More
        </button>
        <Modal isOpen="isOpen" v-if="isOpen" @close="close" :card="card.description" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
      cards: [
        {
          title: "Software Development",
          description:
            "Building robust and scalable software solutions to meet your business needs.",
          image:
            "https://cdn.pixabay.com/photo/2020/09/17/18/05/people-5579977_640.png",
        },
        {
          title: "Web Application Development",
          description:
            "Creating modern and responsive web applications for seamless user experiences.",
          image:
            "https://cdn.pixabay.com/photo/2020/09/17/18/05/people-5579977_640.png",
        },
        {
          title: "Blockchain Development",
          description:
            "Exploring the potential of blockchain technology and developing decentralized applications.",
          image:
            "https://cdn.pixabay.com/photo/2020/09/17/18/05/people-5579977_640.png",
        },
        {
          title: "Trading Bots",
          description:
            "Developing automated trading bots to optimize trading strategies and maximize returns.",
          image:
            "https://cdn.pixabay.com/photo/2020/09/17/18/05/people-5579977_640.png",
        },
        {
          title: "Finance Software Tools Development",
          description:
            "Designing and building software tools for financial analysis, planning, and management.",
          image:
            "https://cdn.pixabay.com/photo/2020/09/17/18/05/people-5579977_640.png",
        },
        {
          title: "Custom Software Solutions",
          description:
            "Tailoring software solutions specifically to your unique business requirements and workflows.",
          image:
            "https://cdn.pixabay.com/photo/2020/09/17/18/05/people-5579977_640.png",
        },
      ],
    };
  },
  methods: {
    close() {
      this.isOpen = false;
    },
  },
};
</script>

<style scoped>
.container {
  padding: 2rem;
}
</style>
